---
layout: post
title: "Git 블로그 입문자를 위한 완벽 정리: 명령어, 구조, CRUD까지"
date: 2025-06-08 21:00:00 +0900
categories: [git, blog, guide]
---

## ✨ 소개

이 글은 **GitHub Pages 블로그를 처음 만드는 사람**을 위해 작성된 실전 가이드용.  
블로그를 만드는 방법부터 글을 쓰고, 수정하고, 삭제하고, 실험용 저장소까지 **모든 Git 기본 사용법**을 총정리.

---git 생성-------

## 📦 1. 저장소 구성

### ✅ GitHub 저장소 2개 생성

| 용도 | 저장소 이름 | 주소 |
|------|--------------|------|
| 블로그 | `subeenyoo777.github.io` | https://subeenyoo777.github.io |
| 테스트 | `sandbox` 또는 `uysb.github.io` | https://subeenyoo777.github.io/sandbox/ |

---

## 🛠 2. GitHub Pages 블로그 만들기

1. GitHub 저장소 만들기 → 이름은 **`username.github.io`**
2. 로컬에서 clone:
   ```bash
   git clone https://github.com/username/username.github.io.git

---
## 3. 초기화
echo "<h1>Hello Blog</h1>" > index.html
git add index.html
git commit -m "Initialize blog"
git push origin main

---
## 4. git 명령어
| 작업    | 명령어                               | 설명                         |
| ----- | --------------------------------- | -------------------------- |
| 상태 확인 | `git status`                      | 변경사항, 스테이징 상태 확인|
| 변경추가  | `git add .` 또는 `git add -A`       | 전체 변경사항 스테이징 |
| 커밋    | `git commit -m "메시지"`             | 변경사항 저장                    |
| 푸시    | `git push origin main`            | GitHub로 업로드                |
| 받기    | `git pull origin main`            | 원격 저장소에서 내려받기              |
| 초기화   | `git init`                    | 로컬 저장소 초기화 (보통 clone으로 대체)|
| 복사    | `git clone URL`                   | 원격 저장소를 로컬에 복제             |
| 주소확인  | `git remote -v`                   | 연결된 원격 저장소 보기            |
| 주소변경  | `git remote set-url origin [URL]` | 저장소 주소 변경                  |


---
## 5. 블로그 글 작성(crud 실습용)
📂 1. _posts 폴더 만들기 (최초 1회만)
mkdir _posts

🆕 마크다운 파일 작성 Create
파일 이름은 반드시 YYYY-MM-DD-title.md 형식으로 작성:
notepad _posts/2025-06-08-my-first-post.md

예시 내용:
---
layout: post
title: "My First Blog Post"
date: 2025-06-08 12:00:00 +0900
categories: [blog, git]
---

이 포스트는 GitHub Pages로 블로그를 운영하기 위한 실전 가이드입니다.


🛠 Update [Git으로 푸시]
(1)파일 열고 내용 수정
(2)Git으로 반영:
git add _posts/2025-06-08-my-first-post.md
git commit -m "Update first post content"
git push origin main

❌ Delete
del _posts/2025-06-08-my-first-post.md
git add -A
git commit -m "Delete first post"
git push origin main


⚙️ 5. _config.yml 예시 
   - Jekyll 설정 파일이 없으면 글이 표시되지 않을 수 있습니다 
title: "Subeen's Dev Blog"
description: "Git, Code, Life."
theme: minima
author: subeenyoo777

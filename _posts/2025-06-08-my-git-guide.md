---
layout: post
title: "Git 블로그 입문자를 위한 완벽 정리: 명령어, 구조, CRUD까지"
date: 2025-06-08 21:00:00 +0900
categories: [git, blog, guide]
---

## ✨ 소개
이 글은 **GitHub Pages 블로그를 처음 만드는 사람**을 위해 작성된 실전 가이드용.  
블로그를 만드는 방법부터 글을 쓰고, 수정하고, 삭제하고, 실험용 저장소까지 **모든 Git 기본 사용법**을 총정리.


---

 # git 명령어
| 작업    | 명령어                               | 설명                         |
| ----- | --------------------------------- | -------------------------- |
| 상태 확인 | `git status`                      | 변경사항, 스테이징 상태 확인|
| 변경추가  | `git add .` 또는 `git add -A`       | 전체 변경사항 스테이징 |
| 커밋    | `git commit -m "메시지`                | 변경사항 저장                  |
| 커밋    | `git commit`                         | 커밋 메세지와 함께 저장          |
| 푸시    | `git push origin main`            | GitHub로 업로드                |
| 받기    | `git pull origin main`            | 원격 저장소에서 내려받기              |
| 초기화   | `git init`                    | 로컬 저장소 초기화 (보통 clone으로 대체)|
| 복사    | `git clone URL`                   | 원격 저장소를 로컬에 복제             |
| 주소확인  | `git remote -v`                   | 연결된 원격 저장소 보기            |
| 주소변경  | `git remote set-url origin [URL]` | 저장소 주소 변경                  |

---

##git 생성

### 📦 1. 저장소 구성

#### ✅ GitHub 저장소 2개 생성

| 용도 | 저장소 이름 | 주소 |
|------|--------------|------|
| 블로그 | `subeenyoo777.github.io` | https://subeenyoo777.github.io |
| 테스트 | `sandbox` 또는 `uysb.github.io` | https://subeenyoo777.github.io/sandbox/ |

---

### 🛠 2. GitHub Pages 블로그 만들기
1. GitHub 저장소 만들기 → 이름은 **`username.github.io`**
2. 로컬에서 clone:
   ```bash
   git clone https://github.com/username/username.github.io.git

---

### 🔄 3. 블로그 초기화: index.html 만들고 올리기

```bash
   # 1. 현재 블로그 저장소 디렉토리로 이동
      cd C:\blog\git\subeenyoo777.github.io

   # 2. index.html 파일 생성
    echo "<h1>Hello Blog</h1>" > index.html

   # 3. Git으로 스테이징
      git add index.html

   # 4. 커밋 메시지와 함께 저장
     git commit -m "Initialize blog"

   # 5. 원격 저장소(GitHub)로 푸시
     git push origin main
```

### 4. 블로그 글 작성(crud 실습용)
#### 📂 1. `_posts` 폴더 만들기 (최초 1회만)

```bash
mkdir _posts
```

#### 🆕 2. 마크다운 글 작성 (Create)
notepad _posts/2025-06-08-my-first-post.md

예시 내용:
---
layout: post
title: "My First Blog Post"
date: 2025-06-08 12:00:00 +0900
categories: [blog, git]
---

파일을 저장한 후, Git으로 등록:

```bash
git add _posts/2025-06-08-my-first-post.md
git commit -m "Add first blog post"
git push origin main
```

#### 🛠 3. 글 수정 (Update)
 1. 파일을 열고 내용 수정
 2. 아래 명령어로 수정 사항 반영:
```bash
git add _posts/2025-06-08-my-first-post.md
git commit -m "Update first post content"
git push origin main
```

#### ❌ 4. 글 삭제 (Delete)
```bash
del _posts/2025-06-08-my-first-post.md
git add -A
git commit -m "Delete first post"
git push origin main
```

#### ⚙️ 5. _config.yml 설정 예시
Jekyll로 블로그 글이 정상적으로 보이게 하려면 _config.yml 파일이 필요합니다.

yaml

title: "Subeen's Dev Blog"
description: "Git, Code, Life."
theme: minima
author: subeenyoo777

작성 후 커밋:
```bash
git add _config.yml
git commit -m "Add site config"
git push origin main
```
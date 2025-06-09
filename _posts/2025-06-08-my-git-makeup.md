---
layout: post
title: "Git 블로그 작성자를 위한 Markdown 꾸미기 문법 가이드"
date: 2025-06-08 23:30:00 +0900
categories: [markdown, guide, blog]
---

GitHub Pages 블로그를 작성할 때 사용하는 문법은 대부분 **Markdown**입니다.  
Markdown은 간단한 기호로 **제목, 목록, 강조, 코드, 링크, 표** 등 다양한 서식을 만들 수 있습니다.  
이 글에서는 Git 블로그에서 가장 많이 사용하는 Markdown 문법을 정리합니다.

---

## 📌 제목 (Heading)

```markdown
# 제목 1
## 제목 2
### 제목 3
#### 제목 4
```

---

## 💬 텍스트 강조
```markdown
**굵게**
*기울임*
~~취소선~~
```

---

## 📝 목록 (List)
순서 있는 목록:
```markdown
1. 첫 번째
2. 두 번째
3. 세 번째

순서 없는 목록:
- 항목 A
- 항목 B
* 항목 C
```

## 💻 코드 (Code)
인라인 코드:
``` markdown
`print("Hello")`
```

## 코드 블록:
<pre> ```python def hello(): print("Hello Git Blog!") ``` </pre>


## 🔗 링크와 이미지
[GitHub](https://github.com)
![이미지설명](https://example.com/image.png)


## 💬 인용문
> 이건 인용문입니다.


## 📊 표 (Table)

| 이름   | 역할     | 비고          |
|--------|----------|---------------|
| subeen | 작성자   | 블로그 운영 중 |
| you    | 독자     | Welcome!       |


## ➖ 수평선 (구분선)

---


## ⚙ Jekyll용 설정(YAML Front Matter)
Markdown 글의 가장 윗부분에는 YAML 설정이 들어갑니다:

---
layout: post
title: "포스트 제목"
date: 2025-06-08 22:00:00 +0900
categories: [blog, example]
---
> 📚Date : 2025.05.13(Tue)

# 한글버전

# 1.Github & Git

## ✅ 1.1 GitHub 레포지토리 연결 확인 방법

### 📁 Git 상태 확인

```bash
git status
```

### 🔗 원격 저장소 확인

```bash
git remote -v
```

출력 예시:

```
origin  https://github.com/yourusername/your-repo.git (fetch)
origin  https://github.com/yourusername/your-repo.git (push)
```

---

## ❗ 1.2 push 시 오류: rejected (fetch first)

### 🔴 에러 메시지

```
! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/...'
```

### 🛠 해결 방법

```bash
git pull origin main --rebase
git push origin main
```

---

## 📁 1.3 workspace 안에 GitHub 파일이 자동 생성된 이유

- `git clone` 혹은 `git pull` 명령으로 GitHub 레포지토리의 내용이 로컬 폴더에 복사되었기 때문
- `.git` 폴더가 있다면 Git 저장소로 초기화된 상태

---

## 🧭 1.4 HEAD -> main, origin/main 의 의미

```plaintext
HEAD -> main, origin/main
```

- `HEAD -> main`: 현재 작업 중인 로컬 브랜치가 main
- `origin/main`: GitHub 상의 main 브랜치
- 두 브랜치가 같은 커밋을 가리키고 있다는 뜻 → 동기화 상태

---

## 🔀 1.5 브랜치 기반 개발 → GitHub → main 병합 워크플로우

### 1. 새 브랜치 생성

```bash
git checkout -b feature/브랜치이름
```

### 2. 작업 및 커밋

```bash
git add .
git commit -m "설명"
```

### 3. GitHub에 브랜치 푸시

```bash
git push origin feature/브랜치이름
```

### 4. GitHub에서 Pull Request 생성 및 병합

### 5. 로컬 main 브랜치 업데이트

```bash
git checkout main
git pull origin main
```

---

## 🗂 1.6 날짜별 폴더 구조 활용

- 예: `workspace/2025-05-13-study/`

```plaintext
workspace/
└── 2025-05-13-study/
    ├── 공부정리.md
    ├── 예제코드.html
    └── 스타일.css
```

- Git에 올리기 편하고 관리하기 깔끔함

---

## 🌿 1.7 브랜치 이름 규칙 (네이밍 컨벤션)

| 유형      | 설명             | 예시                       |
| --------- | ---------------- | -------------------------- |
| feature/  | 새 기능 개발     | feature/login-form         |
| bugfix/   | 버그 수정        | bugfix/button-crash        |
| hotfix/   | 긴급 패치        | hotfix/login-error         |
| docs/     | 문서 관련        | docs/readme-update         |
| refactor/ | 코드 리팩토링    | refactor/component-naming  |
| study/    | 개인 학습 브랜치 | study/2025-05-13-git-study |

---

## 🔁 1.8 pull 이후 main 브랜치로 이동하기

```bash
git checkout main
```

---

## 💬 1.9 VS Code 주석 단축키

| 기능       | Windows / Linux | macOS              |
| ---------- | --------------- | ------------------ |
| 한 줄 주석 | Ctrl + /        | Cmd + /            |
| 블록 주석  | Shift + Alt + A | Shift + Option + A |

---

# 영어 버전

# 1. GitHub & Git

## ✅ 1.1 How to Check GitHub Repository Connection

### 📁 Check Git Status

```bash
git status
```

### 🔗 Check Remote Repository

```bash
git remote -v
```

Example output:

```
origin  https://github.com/yourusername/your-repo.git (fetch)
origin  https://github.com/yourusername/your-repo.git (push)
```

---

## ❗ 1.2 Error When Pushing: rejected (fetch first)

### 🔴 Error Message

```
! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/...'
```

### 🛠 How to Fix

```bash
git pull origin main --rebase
git push origin main
```

---

## 📁 1.3 Why GitHub Files Were Automatically Created in Workspace

- The files were copied to the local folder using `git clone` or `git pull`
- If a `.git` folder exists, it means the directory has been initialized as a Git repository

---

## 🧭 1.4 Meaning of HEAD -> main, origin/main

```plaintext
HEAD -> main, origin/main
```

- `HEAD -> main`: Your current local working branch is `main`
- `origin/main`: The `main` branch on GitHub (remote)
- Both branches point to the same commit → in sync

---

## 🔀 1.5 Branch-Based Development → GitHub → Merge into main Workflow

### 1. Create a New Branch

```bash
git checkout -b feature/branch-name
```

### 2. Make Changes and Commit

```bash
git add .
git commit -m "Description"
```

### 3. Push Branch to GitHub

```bash
git push origin feature/branch-name
```

### 4. Create a Pull Request on GitHub and Merge

### 5. Update Local main Branch

```bash
git checkout main
git pull origin main
```

---

## 🗂 1.6 Using Date-Based Folder Structure

- Example: `workspace/2025-05-13-study/`

```plaintext
workspace/
└── 2025-05-13-study/
    ├── study-notes.md
    ├── example-code.html
    └── style.css
```

- Easy to manage and convenient to upload to Git

---

## 🌿 1.7 Branch Naming Conventions

| Type      | Description             | Example                    |
| --------- | ----------------------- | -------------------------- |
| feature/  | New feature development | feature/login-form         |
| bugfix/   | Bug fixes               | bugfix/button-crash        |
| hotfix/   | Urgent patches          | hotfix/login-error         |
| docs/     | Documentation updates   | docs/readme-update         |
| refactor/ | Code refactoring        | refactor/component-naming  |
| study/    | Personal study branch   | study/2025-05-13-git-study |

---

## 🔁 Switch to main Branch After Pull

```bash
git checkout main
```

---

## 💬 VS Code Comment Shortcuts

| Function      | Windows / Linux | macOS              |
| ------------- | --------------- | ------------------ |
| Line Comment  | Ctrl + /        | Cmd + /            |
| Block Comment | Shift + Alt + A | Shift + Option + A |

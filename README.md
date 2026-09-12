# Daehan Kim — Research Portfolio

정적 HTML/CSS/JS로 만든 개인 연구 포트폴리오 사이트입니다. 빌드 과정 없이 그대로 GitHub Pages에 올릴 수 있습니다.

## 구조

```
portfolio-site/
├── index.html                 메인 페이지 (전체 콘텐츠)
├── style.css                  스타일 (색상/폰트는 :root 변수로 관리)
├── script.js                  모바일 메뉴 토글 등 간단한 JS
├── assets/
│   ├── research-statement-daehan-kim.pdf   원본 연구소개서 (다운로드 링크용)
│   └── img/
│       ├── profile.jpg
│       ├── fig-sensing-1.jpg / fig-sensing-2.jpg
│       ├── fig-wearable.jpg
│       └── fig-semicon-1.jpg / fig-semicon-2.jpg
└── README.md
```

## 로컬에서 미리보기

```bash
cd portfolio-site
python3 -m http.server 8000
# 브라우저에서 http://localhost:8000 접속
```

## GitHub Pages로 배포하기

### 방법 A — 개인 프로필 사이트로 배포 (추천)

`https://<GitHub아이디>.github.io` 주소로 바로 쓰고 싶다면:

```bash
cd portfolio-site
git init
git add .
git commit -m "Initial portfolio site"
git branch -M main
git remote add origin https://github.com/<GitHub아이디>/<GitHub아이디>.github.io.git
git push -u origin main
```

저장소 이름이 정확히 `<GitHub아이디>.github.io`이면, 별도 설정 없이 몇 분 안에
`https://<GitHub아이디>.github.io`에서 바로 접속됩니다.

### 방법 B — 프로젝트 저장소로 배포

아무 이름의 저장소(예: `portfolio`)를 만들고 푸시한 뒤:

1. GitHub 저장소 → **Settings → Pages**
2. **Source**를 `Deploy from a branch`로 설정
3. Branch를 `main`, 폴더를 `/ (root)`로 선택 후 저장

몇 분 후 `https://<GitHub아이디>.github.io/<저장소이름>/`에서 접속할 수 있습니다.

## 아직 채워야 할 부분

`index.html`에서 아래 텍스트를 검색해 실제 정보로 교체하세요 (총 2곳: Hero 섹션, Contact 섹션).

- `your-email@example.com` → 실제 이메일
- `https://github.com/your-username` → GitHub 프로필 주소
- `https://linkedin.com/in/your-profile` → LinkedIn 프로필 주소 (없으면 해당 버튼 `<a>` 태그를 통째로 삭제해도 됩니다)
- `https://scholar.google.com/` → Google Scholar 프로필 주소 (없으면 마찬가지로 삭제 가능)

## 커스터마이징 팁

- **색상**: `style.css` 최상단 `:root { ... }`의 `--navy`, `--accent` 값만 바꾸면 전체 톤이 바뀝니다.
- **논문 추가**: `research-item` 블록을 복사해 새 프로젝트나 출판 논문을 추가할 수 있습니다.
- **사진 교체**: `assets/img/profile.jpg`를 같은 파일명으로 덮어쓰면 됩니다.

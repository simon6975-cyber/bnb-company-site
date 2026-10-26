# 비엔비컴퍼니 (B&B COMPANY) 홈페이지

원두 유통회사 소개 홈페이지 (과제용 시안). 빌드 과정이 없는 정적 사이트라서 Vercel에 그대로 올리면 됩니다.

## 폴더 구성

```
bnb-company-site/
├── index.html          홈페이지 본문 (디자인 · 내용 모두 여기)
├── assets/
│   ├── logo.png        회사 로고
│   ├── favicon.png     브라우저 탭 아이콘
│   └── apple-touch-icon.png  아이폰 홈 화면 아이콘
├── vercel.json         Vercel 설정
└── .gitignore
```

---

## 배포 방법 (GitHub + Vercel, 코딩 없이)

### 1단계. GitHub에 올리기

1. https://github.com 에 로그인 (계정이 없으면 가입)
2. 오른쪽 위 **+** → **New repository**
3. Repository name: `bnb-company-site` 입력 → **Public** 선택 → **Create repository**
4. 생성된 화면에서 **uploading an existing file** 링크 클릭
5. 압축을 푼 `bnb-company-site` 폴더 **안의 내용물 전부**(index.html, assets 폴더, vercel.json, README.md)를 끌어다 놓기
   - 폴더 자체가 아니라 안의 파일들을 올려야 합니다. `index.html`이 맨 위에 보여야 정상입니다.
6. 아래 **Commit changes** 클릭

> 숨김 파일인 `.gitignore`는 안 올라가도 상관없습니다.

### 2단계. Vercel로 배포하기

1. https://vercel.com 접속 → **Continue with GitHub** 로 로그인
2. **Add New… → Project**
3. 목록에서 `bnb-company-site` 옆 **Import**
4. 설정은 건드리지 말고 (Framework Preset: **Other**) **Deploy** 클릭
5. 1분 안에 `https://bnb-company-site.vercel.app` 같은 주소가 생깁니다.

이 주소를 친구에게 보내면 PC · 아이폰 사파리 · 안드로이드 어디서든 똑같이 보입니다.

### 수정하고 싶을 때

GitHub 저장소에서 `index.html` 클릭 → 연필 아이콘(Edit) → 내용 수정 → **Commit changes**
→ Vercel이 자동으로 다시 배포합니다 (1분 정도).

---

## (선택) 터미널을 쓸 줄 안다면

```bash
cd bnb-company-site
git remote add origin https://github.com/<내아이디>/bnb-company-site.git
git branch -M main
git push -u origin main
```

이미 git 저장소로 초기화되어 있고 첫 커밋도 되어 있습니다. push 후 위 2단계(Vercel Import)를 하면 됩니다.

또는 Vercel CLI로 바로 배포:

```bash
npm i -g vercel
cd bnb-company-site
vercel --prod
```

---

## 참고

- 사진은 Unsplash 무료 이미지를 링크로 불러옵니다. 실제 회사 사진으로 바꾸려면 `assets` 폴더에 넣고 `index.html`의 이미지 주소를 `assets/파일이름.jpg`로 바꾸면 됩니다.
- 연혁 · 주요거래처 · 메인 수치 · 사업자등록번호는 예시 내용입니다.
- 문의 폼은 시안용이라 실제로 전송되지는 않습니다 (제출 시 안내 메시지만 표시).

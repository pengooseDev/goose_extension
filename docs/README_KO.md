# Goose Extension Boilerplate

ReactJS + Typescript + Vite 환경의 Google Chrome 확장 프로그램 보일러플레이트입니다. 초기 프로젝트 설정 및 필요한 manifest와 번들링을 위한 rollupOptions이 전부 설정되어있습니다.

## 빠른 시작

저장소 복제:

```bash
git clone https://github.com/pengooseDev/goose_extension.git
```

## 보일러플레이트 사용

크롬 확장 프로그램은 다음과 같은 구성 요소로 이루어져 있습니다.

1. background
2. options
3. popup

구현하고자 하는 기능에 따라 이 파일들을 수정하고 확장할 수 있습니다.

프로젝트는 확장 프로그램을 번들링하기 위해 Vite를 사용합니다.
vite.config.ts의 rollup 설정은 기본적으로 되어있으며, 필요에 따라 설정을 변경할 수 있습니다.

```arduino
src
├─ background
│ ├─ background.html
│ └─ background.ts
├─ options
│ ├─ App.tsx
│ ├─ options.html
│ └─ options.tsx
├─ popup
│ ├─ App.tsx
│ ├─ popup.html
│ ├─ popup.tsx
│ └─ assets
│   └─ logo.ico
└─ manifest.json
```

## 프로덕션 빌드

기능을 구현하였다면 정적 파일로 빌드를 해야합니다.

```bash
npm run build
```

npm run build를 실행한 후, dist 디렉토리는 프로덕션 준비 확장 프로그램을 포함하게 됩니다. 다음의 과정에 따라 정적 파일들을 Chrome에 로드하세요.

- [해당 페이지](chrome://extensions)로 이동하여 확장 관리 페이지를 엽니다.
- Chrome 메뉴를 클릭하고 "도구 더보기" 위로 마우스를 올린 다음 "확장 프로그램"을 선택하여 이 페이지를 엽니다.
- "개발자 모드" 옆에 있는 토글 스위치를 클릭하여 개발자 모드를 활성화합니다.
- "압축해제 된 항목 로드" 버튼을 클릭하고 dist 디렉토리를 업로드합니다.

이제 확장 프로그램이 로드되어 사용 준비가 되었습니다! 😉

## 기여

이 보일러플레이트에 대한 기여를 환영합니다! 변경 사항이나 개선 사항을 제안하려면 pull 요청을 제출하거나 이슈를 열어주세요. 😆

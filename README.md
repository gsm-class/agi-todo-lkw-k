# TODO 앱

배포: https://agi-todo-lkw-k.vercel.app

HTML, CSS, 바닐라 자바스크립트만으로 만든 할 일 관리 앱. 데이터는 브라우저 로컬 스토리지에 저장된다.

## 기능

- 할 일 추가와 삭제
- 체크박스로 완료 상태 전환
- 전체 / 미완료 / 완료 필터
- 미완료 개수 표시
- 로컬 스토리지 저장

## 실행

빌드 과정이 없는 정적 파일이므로 정적 서버만 있으면 된다.

```bash
npx http-server -c-1
```

브라우저에서 http://localhost:8080 을 연다.

## 파일 구성

```
.
├── index.html   # 마크업
├── style.css    # 스타일
└── script.js    # TodoApp 클래스 (상태 관리와 렌더링)
```

## 배포

Vercel에 정적 사이트로 배포한다.

```bash
npx vercel login
npx vercel --prod
```

`.vercelignore`에서 하위 디렉터리를 제외하므로 위 세 파일만 업로드된다.

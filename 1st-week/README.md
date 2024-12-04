# React 프로젝트 세팅 과제 (TypeScript 기반)

## 과제 목적

React 프로젝트를 TypeScript 기반으로 세팅하며 **기본적인 코드 스타일과 퀄리티 유지 방법을 익히고, 팀 협업 및 생산성을 높일 수 있는 환경을 구축**하는 것이 목적입니다.

어떤 설정을 추가했는지 **리드미 파일을 생성**해서 추가한 설정의 의도를 함께 작성해주세요.

<br/>

## 기본 기술 스택

- React
- TypeScript

<br/>

## 필수 구현 사항

### 1. **코드 스타일 정립**

- **ESLint 설정**  
  - TypeScript와 React를 지원하는 ESLint 설정.
  - 필요에 따라 프로젝트에 맞는 추가 규칙 설정.
- **Prettier 설정**  
  - 코드 포맷팅 룰 적용 (e.g., 세미콜론 사용 여부, 탭 너비 설정 등).
  - ESLint와 Prettier 간 충돌 방지를 위한 플러그인 설정.

### 2. **코드 퀄리티 유지**

- **Husky 설정**  
  - Git 훅을 이용하여 커밋 전 특정 명령 실행.
- **Lint-staged 설정**  
  - `pre-commit` 훅에서 실행.
  - 스테이징된 파일에 대해 lint와 포맷팅 실행.
  - TypeScript 파일과 스타일 파일 등 포함.
  - `tsc` 를 활용한 타입스크립트 점검.
- **Commitlint 설정**
  - `commit-msg` 훅에서 실행.
  - 작성된 커밋 형식을 점검하는 명령 실행.

### 3. **스타일링 라이브러리 설정**

- CSS-in-JS 스타일링 라이브러리를 선택하고 프로젝트에 적용.  
  예) `styled-components`, `@emotion/react`, `tailwindcss` 등.

### 4. **전역 상태 관리**

- 전역 상태 관리 라이브러리를 설정하고 샘플 코드를 작성.  
  예) Redux Toolkit, Recoil, Zustand, Jotai 등.

<br/>

## 추가 구현 사항 (선택)

### 1. 프로젝트 디렉토리 구조화

- TypeScript 프로젝트에 적합한 디렉토리 구조 설계.
  ```plaintext
  # 예시 구조
  
  src/
  ├── components/
  ├── pages/
  ├── store/
  ├── styles/
  ├── types/
  └── utils/
  ```

### 2. 테스트 환경 구축

- Jest(혹은 Vitest), React Testing Library 등을 활용하여 테스트 설정.
- TypeScript에 맞는 타입 정의 및 기본 테스트 코드 작성.

### 3. API 연동 및 환경 변수 관리

- `axios` 또는 Fetch API로 HTTP 클라이언트 설정.
- `.env` 파일로 환경 변수를 관리하며 TypeScript로 환경 변수 타입 정의.

### 4. Storybook 설정

- TypeScript와 React를 지원하는 Storybook 설정.
- UI 컴포넌트의 독립적인 개발 및 테스트 환경 구축.

<br/>

## 점검 사항

1. **Lint 및 Prettier 작동 여부 확인**
 
- TypeScript 파일에서 lint와 prettier 규칙 적용 후 자동 수정 여부 테스트.

2. **Git 훅 정상 작동 확인**

 - `pre-commit` 훅에서 `lint-staged` 가 정상적으로 작동하는지 테스트.
   - 타입스크립트 오류가 있는 상황에서 통과되지 않음.
 - `commit-msg` 훅에서 `commitlint` 가 정상적으로 작동하는지 테스트.
   - 커밋 메시지가 `"unknown: hello"` 의 경우엔 통과되지 않지만, `"feat: hello"` 의 경우엔 통과.

3. **스타일링 테스트**

 - 스타일링 라이브러리로 샘플 컴포넌트 제작 후 UI 확인.

4. **전역 상태 관리 테스트**

 - 상태 업데이트 및 공유 로직 샘플을 작성하고 정상 동작 확인.

5. **프로젝트 실행 확인**

 - `npm start` 또는 `yarn start` 명령으로 개발 서버 실행 확인.

6. **타입스크립트 타입 검사**

 - 프로젝트의 `tsconfig.json` 설정 확인 및 `tsc` 명령으로 타입 검사 실행.

<br/>

## 제출 요구 사항

1. GitHub에 세팅된 개인 폴더에 프로젝트 업로드.
2. 프로젝트의 주요 설정 및 사용 방법을 명시한 `README.md` 파일 포함.
3. 필수 구현 사항을 충족하며, 선택적으로 추가 구현 사항을 포함.

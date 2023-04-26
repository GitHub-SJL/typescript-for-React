# TypeScript for React

React 라이브러리 사용 시 Typescript 초기 설정 방법

## TypeScript 설정

1.  기존 Create React App으로 만든 프로젝트에 타입스크립트 설치

`npm install --save typescript @types/node @types/react @types/react-dom @types/jest`
+tsconfig.json파일이 없다면 추가로 설정

2.  Create React App을 타입스크립트로 시작하기

`npx create-react-app my-app --template typescript` 또는
You are running create-react-app 4.0.3, which is behind the latest release (5.0.0).
오류가 뜬다면 `npx create-react-app` 명령어로 진행

## Styled Components 설치

어떤 라이브러리나 패키지는 TypeScript로 만들어진게 아니고 JavaScript 기반으로 만들어졌다.
그래서 TypeScript는 타입을 모르고 코드가 실행되기 전에 알아야할 필요가 있다.

styled-components 같은 경우
`npm i @types/styled-components` 명령어를 통해 타입이 선언된 라이브러리를 설치할수 있다.
따라서 패키지를 설치하고 이러한 type 정의가 된 패키지를 추가로 설치해야 타입스크립트에서 정상적으로 사용할수 있다.

DefinitelyTyped (type이 정의된 수많은 라이브러리가 모여있음)
https://github.com/DefinitelyTyped/DefinitelyTyped

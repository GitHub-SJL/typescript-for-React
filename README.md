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

## props에 타입 설정

inteface object를 통해 type을 미리 지정해주기

## Optional Props

?를 통해 property의 필수가아닌 선택으로 지정가능

대신 컴포넌트랑 스타일드 컴포넌트랑 옵션인지 필수인지 맞춰야함

**?? (Null 병합 연산자 (Nullish coalescing operator))**

??앞에 값이 null이거나 undefined이면 오른쪽 값을, 그렇지 않으면 왼쪽 값을 반환하는 논리연산자

**default 값 주기**
타입스크립트 뿐만아니라 ES6 기본문법도 활용하기

## State

useState < number > ( )

state의 type을 지정하려면 Generics안에 타입을 지정

일반적으로는 초기값을 지정하면 타입스크립트가 자동으로 타입을 유추하기 때문에 굳이 지정해주지 않아도 되지만 상태가 undefined또는 null이 될 수도 있거나 객체 또는 배열일 때는 지정해주는 것이 좋다.

ex)
const [ value, setValue ] = useState< Value | null >(null);

## Forms

React.FormEvent HTMLInputElement
onChange 함수가 inputElement에 의해서 실행 될것을 알게된다.
React.FormEvent HTMLFormElement
onSubmit 함수가 formElement에 의해서 실행 될것을 알게된다.

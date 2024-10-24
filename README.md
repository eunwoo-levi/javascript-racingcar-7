# **🏎️ 자동차 경주 게임**

# 📌 과제 진행 요구 사항

- 미션은 자동차 경주 저장소를 포크하고 클론하는 것으로 시작한다.
- 기능을 구현하기 전 README.md에 구현할 기능 목록을 정리해 추가한다.
- Git의 커밋 단위는 앞 단계에서 README.md에 정리한 기능 목록 단위로 추가한다.
  - AngularJS Git Commit Message Conventions을 참고해 커밋 메시지를 작성한다.
- 자세한 과제 진행 방법은 프리코스 진행 가이드 문서를 참고한다.

# 📂 폴더 구조

```
📦src
┣ 📂constants      // 애플리케이션 전역에서 사용되는 상수 정의
┃ ┣ 📜errors.js    // 에러 메시지 상수
┃ ┗ 📜messages.js  // UI 메시지 상수
┣ 📂views          // 사용자 입출력 처리 뷰 컴포넌트
┃ ┣ 📜InputView.js // 사용자 입력을 처리하는 뷰
┃ ┗ 📜OutputView.js// 결과 출력을 처리하는 뷰
┣ 📂models         // 데이터와 비즈니스 로직을 처리하는 모델
┃ ┣ 📜Car.js  // 자동차 데이터 모델
┃ ┗ 📜Game.js // 게임 상태와 로직 모델
┣ 📂controllers    // 애플리케이션 흐름을 제어하는 컨트롤러
┃ ┗ 📜GameController.js // 게임 진행을 제어하는 컨트롤러
┣ 📂utils          // 공통 유틸리티 기능 모음
┃ ┗ 📜validators.js// 입력값 검증 유틸리티
┣ 📜App.js         // 애플리케이션의 초기화 담당
┗ 📜index.js       // 애플리케이션 진입점
```

# 구현 외 목표

- 1.  Airbnb 자바스크립트 스타일 가이드 정독
- 2.  AngularJS Git Commit Message Conventions 정독
- 3.  JEST 3가지 문서 정독

# 📝 구현할 기능 목록

# 🏎️ 자동차 경주 게임

## 📋 구현할 기능 목록

### 1. 입력 기능

#### 1.1. 자동차 이름 입력 ✅

- [x] 쉼표(,)를 기준으로 자동차 이름을 입력 받는다
- [x] 입력받은 문자열을 쉼표 기준으로 분리한다
- [x] 각 이름의 앞뒤 공백을 제거한다
- [x] 빈 문자열 검사를 수행한다

#### 1.2. 자동차 이름 유효성 검사 ✅

- [x] 각 자동차 이름이 5자 이하인지 검사한다
- [x] 이름이 공백인 경우 에러를 발생시킨다
- [x] 이름이 중복되는 경우 에러를 발생시킨다

#### 1.3. 시도 횟수 입력 ✅

- [x] 시도할 횟수를 입력 받는다
- [x] 입력값이 숫자인지 검사한다
- [x] 입력값이 0 이상인지 검사한다

### 2. 자동차 기능

#### 2.1. 자동차 생성 ✅

- [ ] 입력받은 이름으로 자동차 객체를 생성한다
- [ ] 자동차의 초기 위치를 0으로 설정한다
- [ ] private 필드를 사용하여 데이터 보호

#### 2.2. 자동차 이동 ✅

- [ ] 0-9 사이의 무작위 값을 생성한다
- [ ] 무작위 값이 4 이상인 경우 전진한다
- [ ] 전진 시 위치를 1 증가시킨다

### 3. 게임 진행 기능

#### 3.1. 게임 초기화 ✅

- [ ] 입력받은 자동차들을 저장한다
- [ ] 게임 시도 횟수를 저장한다
- [ ] private 필드를 사용하여 데이터 보호

#### 3.2. 라운드 진행 ✅

- [ ] 입력받은 횟수만큼 라운드를 반복한다
- [ ] 각 라운드마다 모든 자동차를 이동시킨다
- [ ] 각 라운드의 실행 결과를 출력한다

### 4. 출력 기능

#### 4.1. 중간 결과 출력 ✅

- [ ] 각 자동차의 이름을 출력한다
- [ ] 자동차의 위치를 '-' 문자로 표현한다
- [ ] 각 라운드마다 모든 자동차의 상태를 출력한다

#### 4.2. 최종 우승자 출력 ✅

- [ ] 가장 멀리 이동한 거리를 구한다
- [ ] 최대 거리만큼 이동한 자동차들을 찾는다
- [ ] 우승자가 여러 명인 경우 쉼표(,)로 구분하여 출력한다

### 5. 예외 처리

#### 5.1. 입력값 예외 ✅

- [ ] "[ERROR]"로 시작하는 에러 메시지를 출력한다
- [ ] 자동차 이름이 5자 초과시 에러 발생
- [ ] 자동차 이름이 빈 문자열일 경우 에러 발생
- [ ] 자동차 이름이 중복될 경우 에러 발생

#### 5.2. 시도 횟수 예외 ✅

- [ ] 시도 횟수가 숫자가 아닐 경우 에러 발생
- [ ] 시도 횟수가 양의 정수가 아닐 경우 에러 발생

### 6. 테스트 (진행중)

#### 6.1. 기본 테스트코드 통과 (TODO)

- [ ] 기능 테스트
- [ ] 예외 테스트

#### 6.2. 추가 테스트 작성 (TODO)

- [ ] 입력값 경계 테스트
  - [ ] 정확히 5글자인 이름
  - [ ] 1회 시도
- [ ] 게임 진행 테스트
  - [ ] 단일 우승자 케이스
  - [ ] 공동 우승자 케이스
  - [ ] 여러 라운드 진행 케이스
- [ ] 예외 처리 테스트
  - [ ] 자동차 이름 5자 초과
  - [ ] 빈 문자열 이름
  - [ ] 잘못된 시도 횟수 입력
  - [ ] 음수 시도 횟수

### 추가된 개선사항 ✅

- [x] 클래스의 private 필드/메서드 사용으로 캡슐화
- [x] MVC 패턴 적용
- [x] 입력과 출력의 책임 분리
- [x] 상수 분리 및 관리

# 📋 기능 요구 사항

**초간단 자동차 경주 게임을 구현한다.**

- 주어진 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다.
- 각 자동차에 이름을 부여할 수 있다. 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
- 자동차 이름은 쉼표(,)를 기준으로 구분하며 이름은 5자 이하만 가능하다.
- 사용자는 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.
- 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4 이상일 경우이다.
- 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.
- 우승자가 여러 명일 경우 쉼표(,)를 이용하여 구분한다.
- 사용자가 잘못된 값을 입력할 경우 "[ERROR]"로 시작하는 메시지와 함께 Error를 발생시킨 후 애플리케이션은 종료되어야 한다.

## 입출력 요구 사항

### 입력

- 경주할 자동차 이름(이름은 쉼표(,) 기준으로 구분)

```
pobi,woni,jun
```

- 시도할 횟수

```
s
```

### 출력

- 차수별 실행 결과

```
pobi : --
woni : ----
jun : ---
```

- 단독 우승자 안내 문구

```
최종 우승자 : pobi
```

- 공동 우승자 안내 문구

```
최종 우승자 : pobi, jun
```

### 💻 실행 결과 예시

```
경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)
pobi,woni,jun
시도할 횟수는 몇 회인가요?
5

실행 결과
pobi : -
woni :
jun : -

pobi : --
woni : -
jun : --

pobi : ---
woni : --
jun : ---

pobi : ----
woni : ---
jun : ----

pobi : -----
woni : ----
jun : -----

최종 우승자 : pobi, jun
```

# 🔍 프로그래밍 요구 사항

- Node.js 20.17.0 버전에서 실행 가능해야 한다.
- 프로그램 실행의 시작점은 App.js의 run()이다.
- package.json 파일은 변경할 수 없으며, 제공된 라이브러리와 스타일 라이브러리 이외의 외부 라이브러리는 사용하지 않는다.
- 프로그램 종료 시 process.exit()를 호출하지 않는다.
- 프로그래밍 요구 사항에서 달리 명시하지 않는 한 파일, 패키지 등의 이름을 바꾸거나 이동하지 않는다.
- 자바스크립트 코드 컨벤션을 지키면서 프로그래밍한다.
  - 기본적으로 JavaScript Style Guide를 원칙으로 한다.

# 🔍 프로그래밍 요구 사항 2

- indent(인덴트, 들여쓰기) depth를 3이 넘지 않도록 구현한다. 2까지만 허용한다.
  - 예를 들어 while문 안에 if문이 있으면 들여쓰기는 2이다.
  - 힌트: indent(인덴트, 들여쓰기) depth를 줄이는 좋은 방법은 함수(또는 메서드)를 분리하면 된다.
- 3항 연산자를 쓰지 않는다.
- 함수(또는 메서드)가 한 가지 일만 하도록 최대한 작게 만들어라.
- Jest를 이용하여 정리한 기능 목록이 정상적으로 작동하는지 테스트 코드로 확인한다.
  - 테스트 도구 사용법이 익숙하지 않다면 아래 문서를 참고하여 학습한 후 테스트를 구현한다.
    - Using Matchers
    - Testing Asynchronous Code
    - Jest로 파라미터화 테스트하기: test.each(), describe.each()

## 라이브러리

- @woowacourse/mission-utils에서 제공하는 Console API를 사용하여 구현해야 한다.
  - Random 값 추출은 Random.pickNumberInRange()를 활용한다.
  - 사용자의 값을 입력 및 출력하려면 Console.readLineAsync()와 Console.print()를 활용한다.

# 202130310 신동주
# 6주차 (2023 04 06)

컴포넌트 추출
  - 큰 컴포넌트에서 일부를 추출해서 새로운 컴포넌트를 만드는 것
  - 기능 단위로 구분하는 것이 좋고, 나중에 곧바로 재사용이 가능한 형태로 추출하는 것이 좋음
 
State
  - State란?
     1. 리액트 컴포넌트의 변경 가능한 데이터
     2. 컴포넌트를 개발하는 개발자가 직접 정의해서 사용
     3.  atete 가 변경될 경우 컴포넌트가 재렌더링됨
     4.  렌더링이나 데이터 흐름에 사용되는 값만 state에 포함시켜야 함

  - State의 특징
     1. 자바스크립트 객체 형태로 존재
     2. 직접적인 변경이 불가능 함
     3. 클래스 컴포넌트
      3-1. 생성자에서 모든 state를 한번에 정의
      3-2. state를 변경하고자 할 때에는 꼭 set State()함수를 사용해야 함
     4. 함수 컴포넌트
      4-1. useState()훅을 사용하여 각각의 state를 정의
      4-2. 각 state별로 주어지는 set함수를 사용하여 state 값을 변경

생명주기
   - 마운트
     1. 컴포넌트가 생성될 떼
     2. componentDidMount()

   - 업데이트
     1. 컴포넌트의 props가 변경될 때
     2. setState() 함수 호출에 의해 state가 변경될 때
     3. forceUpdate()라는 강제 업데이트 함수가 호출될 때
     4. componentDidUpdate()
   
   -  언마운트
     1. 상위 컴포넌트에서 현재 컴포넌트를 더 이상 화면에 표시하지 않게 될 때
     2. componentWillUnmount()
   
   - 컴포넌트는 계속 존재하는 것이 아니라 시간의 흐름에 따라 생성되고 업데이트되다가 사라지는 과정을 겪음
    


# 5주차 (2023 03 30)

리액트 컴포넌트
- 컴포넌트 기반 구조
   1. 작은 컴포넌트들이 모여서 하나의 컴포넌트를 구성하고 이러한 컴포넌트들이 모여서 전체 페이지를 구성
- 개념적으로는 자바스크립트의 함수와 비슷함
   1. 속성들을 입력으로 받아서 그에 맞는 리액트 엘리먼트를 생성하여 리턴함

Props
 - Props의 개념
   1. 리액트 컴포넌트의 속성
   2. 컴포넌트에 전달할 다양한 정보를 담고 있는 자바스크립트 객체
   
 - Props의 특징
   1. 읽기 전용
   2. 리액트 컴포넌트의 props는 바꿀 수 없고, 같은 props가 들어오면 항상 같은 엘리먼트를 리턴해야 함
   
 - Props 사용법
   1. JSX를 사용할 경우 컴포넌트에 키-값 쌍 형태로 넣어 주면 됨
   2. 문자열 이외에 정수,변수,그리고 다른 컴포넌트 등이 들어갈 경우에는 중괄호를 사용해서 감싸주어야 함
   3. JSX를 사용하지 않는 경우에는 createElement() 함수의 두 번째 파라미터로 자바스크립트 객체를 넣어 주면 됨

엘리먼트에 대해 배웠다
- 엘리먼트
   엘리먼트의 정의
   1. 리액트 앱의 가장 작은 빌딩 블록들
   2. 화면에 나타나는 내용을 기술하는 자바스크립트 객체
   3. 리액트 엘리먼트는 DOM 엘리먼트의 가상 표현

  엘리먼트의 생김새
   1. 엘리먼트는 자바스크립트 객체 형태로 존재
   2. 컴포넌트 유형과 속성 및 내부의 모든 자식에 대한 정보를 포함하고 있는 일반적인 자바스크립트 객체

  엘리먼트의 특징
   1. 불변성을 갖고 있음
   2. 엘리먼트 생성 후에는 자식이나 속성을 바꿀 수 없음

- 엘리먼트 렌더링하기
   렌더링을 위해 ReactDom의 render()라는 함수를 사용
    1. 리액트 엘리먼트를 HTML 엘리먼트에 렌더링하는 역할
   렌더링 되는 과정은 Victual DOM에서 실제 DOM으로 이동하는 과정
- 렌더링된 엘리먼트 업데이트하기
    엘리먼트는 한 번 생성되면 바꿀 수 없기 때문에 엘리먼트를 업데이트하기 위해서는 다시 생성해야 함
    기존 엘리먼트를 변경하는 것이 아니라 새로운 엘리먼트를 생성해서 바꿔치기하는 것


# 4주차 (2023 03 23)

git hub에 리액트를 직접 연결했다.
기존  respository를 삭제하고 새로운 respository를 생성했다.

JSX는 자바스크립트와 XML/HTML을 함께 사용할 수 있는 자바스크립트의 확장 문법이다.

JSX의 역할은 2가지가 있는데 첫번째는 JSX로 작성된 코드를 자바스크립트 코드로 변환하는 역할과 두번째는 리액트가 JSX코드를 모드 createElement() 함수를 사용하는 코드로 변환시키는 역할을 한다.

JSX의 장점
  1. 코드가 간결해진다.
  2. 가독성이 좋아진다.
  3. Injection Attack을 방어함으로써 보안성이 올라갔다. 

JSX 사용법
  1. 기본적으로 모든 자바스크립트 문법을 지원
  2. 자바스크립트에 XML과 HTML을 섞어서 사용한다
  3. 중괄호를 사용하여 자바스크립트 코드를 삽입한다. 

# 3주차 (2023.03.16)

Node.js를 설치했다,그리고 버전을 확인 했다.

리액트는 사용자와 웹사이트의 상호작용을 돕는 인터페이스를 만들기 위한 자바스크립트 기능 모음집이다.

리액트의 장점
1. 빠른 업데이트와 렌더링 속도
2. 컴포넌트 기반의 구조
3. 높은 재사용성
4. 몇 년 동안 지속될 영향력
5. 활발한 지식 공유 $ 커뮤니티
6. 모바일 앱 개발 가능

리액트의 단점
1. 방대한 학습량
2. 높은 상태 관리 복잡도

# 2주차 (2023.03.09)

깃 허브 계정을 만들고  23-React1라는 이름의 repository를 추가했다.

깃 허브는 다수가 동시에 사용할 수 있는 사이트이다.

깃 허브 주소를 복사하고 공유하는 사이트에 올렸다.

웹 기본 연결 브라우저를 인터넷 익스플로어에서 크롬으로 변경했다.

깃 이그노어는 깃 허브의 공유과정에서 생기는 문제를 방지해주기 위한 파일이다.


# 1주차 (2023.03.02)
> 오리엔테이션
> github 가입
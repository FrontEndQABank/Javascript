# 🙋‍Javascript 기술 면접 질문
💥이모티콘이 있는 질문은 면접에서 받았던 질문입니다.

<br>

> 프로그래밍

<details>
<summary>프로그래밍이란 뭐라고 생각하나요?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>컴파일러는 뭐고 인터프리터는 뭔가요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 변수

<details>
<summary>호이스팅이 뭔가요?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>let 키워드는 var 키워드와 어떤 점이 다른가요?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>const 키워드는 어떤 특징이 있나요?💥</summary>
<div markdown="1">
1. 선언과 초기화
const 키워드로 선언한 변수는 선언과 동시에 초기화가 이루어져야 합니다.
2. 재할당 금지
var 또는 let 키워드로 선언한 변수는 재할당이 자유로우나 const 키워드로 선언한 변수는 재할당이 안됩니다.
3. 상수(변하지 않는 변수)
const로 선언한 변수에 원시 값을 할당한 경우 변수 값을 변경할 수 없습니다.
원시 값은 변경 불가능한 값이기 때문입니다. 이러한 특징을 사용하여 상수로 표현합니다.
</div>
</details>

<details>
<summary>식별자 네이밍 규칙은 어떤 것들이 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>데이터 타입의 종류는 어떤 것들이 있나요?💥</summary>
<div markdown="1">
원시 타입과 객체 타입이 있습니다. 원시 타입으로는 string(문자), Boolean(참과 거짓), number(숫자), null(의도적으로 값이 없음), undefined(값이 할당되지 않음), symbol(유일무이한 값), BigInt(아주 큰 정수)가 있습니다. 원시 타입을 제외한 모든 것은 다 객체 타입입니다. 배열, 함수, 객체가 있습니다. 이러한 데이터 타입은 자바스크립트에서 사용되며, 각각 다른 특징과 용도로 쓰이고 있습니다. 원시 타입은 값에 의한 전달로 동작하고, 객체 타입은 참조에 의한 전달로 동작합니다.
</div>
</details>

<details>
<summary>데이터 타입은 왜 필요할까요?</summary>
<div markdown="1">
1. 값을 저장할때 확보해야하는 메모리 공간의 크기를 결정하기 위해 필요합니다.<br>
2. 값을 참조할 때 읽어들여야 하는 메모리 공간의 크기를 결정하기 위해 필요합니다.<br>
3. 메모리에서 읽어들인 2진수를 어떻게 해석해야 할지 결정하기 위해 필요합니다.<br>
  <br>
  <details>
  <summary>보충 설명</summary>
<div markdown="1">
1.값을 저장할때 확보해야 하는 메모리 공간의 크기를 결정하기 위해 필요합니다. <br>
a라는 이름으로 공간을 만들었습니다. a공간에 2진수 형태로 데이터를 저장합니다.
이 과정에서 우리가 직접 얼마의 메모리 공간을 확보해야하는지 명시해주지 않아도 됩니다.
자바스크립트 엔진은 데이터 타입에 따라 알맞은 크기의 메모리 공간을 확보해주기 때문입니다.<br>
<br>
2.값을 참조할때 읽어들여야 하는 메모리 공간의 크기를 결정하기 위해 필요합니다.<br>
a변수를 통해 50이라는 값이 저장되어 있는 메모리 공간을 찾아갈 수 있습니다. 이때 값을
참조하기 위해서는 한번에 읽어들여할 메모리 크기를 알아야 합니다. a변수의 경우, 저장되어 있는 값이
숫자타입이므로 8바이트 단위로 읽지 않으면 원하는 값을 얻어낼 수 없습니다.
그렇다면 컴퓨터는 어떻게 한 번에 읽어들일 메모리의 크기를 알아낼 수 있을까요?
자바스크립트 엔진은 a 변수에 숫자타입의 값이 할당되어있기 때문에 a변수를 숫자타입으로 인식합니다.
숫자 타입은 8바이트 단위로 저장되므로 a변수를 참조하면 8바이트 단위로 메모리를 읽어들여 값을 얻어낼수 있습니다.
이처럼 어떤 데이터를 참조하는 과정에서 얼마의 메모리 공간을 읽어 들일지 알기 위해 데이터타입이 필요합니다.
<br>
  <br>
3.메모리에서 읽어들인 2진수를 어떻게 해석해야 할지 결정하기 위해 필요합니다.<br>
a변수 값을 사용할려고 가져왔더니 2진수 형태로 저장되어 있습니다.
이는 숫자일수도 있고 문자일수도 있습니다. 이때 2진수를 어떻게 해석할지 결정하는 방법으로
데이터 타입이 쓰입니다.</div>
  </details>
  
</div>
</details>

<details>
<summary>명시적 타입 변환 함수를 예를 들어볼 수 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>truthy / falsy 한 값이 뭔가요?💥</summary>
<div markdown="1">
turthy 값은 참으로 평가되는 값으로 true, 빈배열, 빈객체, 1 등이 있으며, falsy 값은 거짓으로 평가되는 값으로 false, undefined, null, 0, -0이 있습니다.
</div>
</details>

<br>

> 배열

<details>
<summary>배열의 메서드는 어떤 종류가 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>고차 함수에 대해서 아나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>forEach 메서드와 map메서드의 차이점은?💥</summary>
<div markdown="1">
forEach 는 별도의 반환값이 없이 배열 원소를 처음부터 끝까지 순회하는 메서드이며, map은 새 배열을 반환한다는 점에 차이가 있습니다.
</div>
</details>

<br>

> 구조 분해 할당

<details>
<summary>구조 분해 할당이 뭔가요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>구조 분해 할당은 크게 어떤 종류가 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 브라우저 렌더링 과정

<details>
<summary>브라우저의 렌더링 과정에 대해 설명해보세요💥</summary>
<div markdown="1">
0. 서버에 필요한 리소스를 요청합니다. 서버는 브라우저에게 필요한 HTML을 보내줍니다.<br>
1. HTML 파일을 받은 브라우저는 파싱하며 DOM트리를 생성합니다.<br>
2. HTML을 읽는 중 CSS 요청이 발생하면 CSS 파일을 받아와 CSSOM 트리를 생성합니다.<br>
3. JavaScript 코드를 만나면 HTML 파싱을 중단하고 제어권한을 JavaScript 엔진에게 넘깁니다. JavaScript 코드를 파싱하고 실행합니다.<br>
4. DOM 트리와 CSSOM 트리를 결합하여 렌더 트리(Render Tree)를 생성합니다. 렌더 트리는 화면에 실제로 표시될 요소들로 구성됩니다.<br>
5. 렌더 트리의 각 노드에 대해 위치와 크기를 계산하는 레이아웃(Layout) 단계가 발생합니다.<br>
6. 레이아웃 단계에서 계산된 위치와 크기를 실제 픽셀로 변환하여 화면에 출력합니다. 이를 페인트(Paint)라고 합니다.<br>
7. Composition 단계에서는 레이아웃과 페인트를 수행하지 않고 레이어의 합성만 실행합니다. 이 단계에서는 transform, opacity와 같은 요소들이 처리됩니다.이러한 과정을 통해 HTML, CSS, JavaScript를 조합하여 브라우저에서 웹 페이지를 렌더링하고 화면에 표시됩니다.<br>
<br>
***리플로우와 리페인트가 무엇인가요? <br>
HTML의 레이아웃이 변경될 경우 레이아웃 단계에서 렌더트리가 재생성되어 리플로우가 실행됩니다.
레이아웃과 관련없는 스타일이 변경될 경우에는 체인트 단계가 다시 실행되어 리페인트가 실행됩니다.
</div>
</details>

<details>
<summary>브라우저의 렌더링 과정에 자바스크립트는 어떻게 동작하나요?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary><script></script> 태그를 <body></body> 태그 밑에 둬야하는 이유가 있을까요? </summary>
<div markdown="1">
답변을 HTML 파서는 <script> 태그를 만나면 파싱을 멈추고 스크립트 파일을 읽기 때문에 HTML 코드 중간에 <script> 태그가 있으면 무거운 JavaScript 코드를 불러오고 실행하느라 DOM 생성이 지연됩니다.
DOM 생성이 지연되면 브라우저 렌더링에 방해가 되므로 미완성 화면이 오래 유지될 수 있습니다.
따라서 <script> 태그는 HTML 코드를 모두 작성 후 <body> 태그 닫기 직전에 작성하는 것이 좋습니다.
</div>
</details>

<br>

> 브라우저 렌더링 과정

<details>
<summary>DOM이 뭔가요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>DOM을 구성하는 건 뭐가 있나요? </summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 이벤트

<details>
<summary>이벤트 핸들러를 등록하는 방식에는 어떤 것들이 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>이벤트 전파(propagation)에 대해서 알고 있나요?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>이벤트 위임(delegation)에 대해서 알고있나요?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>e.preventDefault에 대해 알고 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>e.stopPropagation에 대해 알고 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 객체 리터럴

<details>
<summary>함수와 메서드의 차이점에 대해 알고 계신가요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>자바스크립트에서 객체를 생성하는 방법은 어떤 것들이 있나요? </summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 원시 값과 객체 비교

<details>
<summary>동적 타이핑을 지원하는 자바스크립트에서 데이터의 타입을 크게 2개로 나누는 이유가 있을까요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>값에 의한 전달이 뭔가요?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>참조에 의한 전달이 뭔가요?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 함수

<details>
<summary>자바스크립트에서 함수를 정의하는 방법은 몇가지가 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>함수 선언문과 함수 표현식은 어떤 차이가 있나요? </summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>즉시 실행 함수(IIFE)에 대해 알고 있나요? 알고 있다면 아는 내용에 대해 말해보세요</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 스코프

<details>
<summary>스코프가 뭔가요?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>스코프에는 어떤 종류가 있죠?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>렉시컬 스코프를 아나요? 안다면 렉시컬 스코프는 무엇을 의미하나요?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>전역 변수로 변수를 선언하면 생기는 문제점은 무엇이 있을까요?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 생성자 함수

<details>
<summary>객체 리터럴로 만들 때와는 무슨 차이가 있죠? 왜 생성자 함수를 사용하나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>생성자 함수가 객체(인스턴스)를 생성하는 과정에 대해 간략하게 설명해줄 수 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 함수와 일급 객체

<details>
<summary>일급 객체가 뭔가요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>자바스크립트에서 함수가 일급 객체라면, 일급 객체로 뭘 할 수 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>함수형 프로그래밍이 뭔가요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>순수 함수가 뭔가요? 일반 함수와는 어떤 차이가 있죠?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 객체지향 프로그래밍

<details>
<summary>객체지향 프로그래밍은 무엇을 의미하나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>객체지향 프로그래밍의 특징에 대해 말해볼 수 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>프로토타입이 뭔가요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> strict mode

<details>
<summary>strict mode가 뭔가요? </summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>strict mode를 통해 무엇을 예방할 수 있죠? </summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 빌트인 객체

<details>
<summary>빌트인 객체가 뭔가요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>빌트인 객체의 종류는 어떤게 있죠?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>래퍼 객체에 대해서 알고 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> this

<details>
<summary>this가 뭔가요?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>this 바인딩이란?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>this는 동적으로 바인딩이 된다고 하는데 바인딩되는 객체가 어떻게 다르나요?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 실행 컨텍스트

<details>
<summary>실행 컨텍스트에 대해 말해보세요</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 클로저

<details>
<summary>클로저에 대해서 아나요?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>클로저를 사용하면 뭐가 좋죠?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>클로저를 어떻게 생성하나요?💥</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 클래스

<details>
<summary>그럼 생성자 함수와 클래스는 어떤 차이가 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>클래스 정의</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>클래스 상속</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 스프레드 문법

<details>
<summary>spread 문법이 뭔가요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>어떤 상황에서 사용할 수 있죠?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

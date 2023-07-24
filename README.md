# 🙋‍Javascript 기술 면접 질문

💥이모티콘이 있는 질문은 면접에서 받았던 질문입니다.

<br>

> 프로그래밍

<details>
<summary>프로그래밍이란 뭐라고 생각하나요?💥</summary>
<div markdown="1">
프로그래밍이란 구현하고자 하는 요구사항을 컴퓨터가 이해할 수 있도록 정확하고 상세하게 요구를 설명하는 작업입니다.
</div>
</details>

<details>
<summary>컴파일러는 뭐고 인터프리터는 뭔가요?</summary>
<div markdown="1">
컴파일러와 인터프리터는 작성한 코드를 기계어로 번역해주는 번역기 입니다. 컴파일러는 프로그램 전체를 스캔하여 번역해주는 방식이며, 실행파일이 생성됩니다. Java, C 등이 이 방식을 사용합니다. 컴파일 하기 전 스캔단계에서 오류를 캐치할 수 있는 특징이 있습니다.
인터프리터는 프로그램 실행 시 한줄 씩 번역하는 방식으로 JS, Python 등이 있습니다. 프로그램을 실행해야만 오류를 잡아낼 수 있는 특징이 있습니다.
</div>
</details>

<br>

> 변수

<details>
<summary>호이스팅이 뭔가요?💥</summary>
<div markdown="1">
자바스크립트 엔진은 소스코드를 순차적으로 실행하기에 앞서 선언문(변수 선언문, 함수 선언문 등)을 먼저 실행합니다. 변수 선언이 소스코드의 어디에 위치하는지와 상관없이 어디서든지 변수를 참조할 수 있습니다. 이처럼 변수 선언문이 코드의 선두에 끌어 올려진 것처럼 동작하는 자바스크립트 고유의 특징을 변수 호이스팅이라고 합니다.    
</div>
</details>

<details>
<summary>let 키워드는 var 키워드와 어떤 점이 다른가요?💥</summary>
<div markdown="1">
1. let은 블록스코프를 가지고 있고 var키워드는 함수스코프를 가지고 있습니다. <br/>
2. let은 재할당만 가능하지만 var는 재선언, 재할당이 모두 가능합니다.<br/>
3. var는 선언과 동시에 undefined로 초기화가 되지만 let은 선언과 초기화가 분리되어 초기화가 되기전에 변수를 호출하면 ReferenceError가 발생합니다.<br>
4. let은 변수 호이스팅이 일어나지 않는 것 처럼 동작합니다.<br/>
5. let은 전역 객체로 접근할 수 없습니다.<br/>
<b>[추가 TDZ]</b> <br/>
"let" 및 "const" 키워드로 선언된 변수는 TDZ(Temporary Dead Zone)에 영향을 받습니다. TDZ는 변수가 선언되었지만 초기화되기 전까지 액세스할 수 없는 구간을 의미합니다. 따라서 선언 이전에 "let" 또는 "const" 변수를 사용하면 ReferenceError가 발생합니다. 이와는 달리 "var" 키워드로 선언된 변수나 함수 선언은 TDZ에 영향을 받지 않으므로, 선언 이전에도 참조할 수 있습니다.
</div>
</details>

<details>
<summary>const 키워드는 어떤 특징이 있나요?💥</summary>
<div markdown="1">
1. 선언과 초기화<br>
const 키워드로 선언한 변수는 선언과 동시에 초기화가 이루어져야 합니다.<br><br>
2. 재할당 금지<br>
var 또는 let 키워드로 선언한 변수는 재할당이 자유로우나 const 키워드로 선언한 변수는 재할당이 안됩니다.<br><br>
3. 상수(변하지 않는 변수)<br>
const로 선언한 변수에 원시 값을 할당한 경우 변수 값을 변경할 수 없습니다.<br>
원시 값은 변경 불가능한 값이기 때문입니다. 이러한 특징을 사용하여 상수로 표현합니다.<br>
</div>
</details>

<details>
<summary>식별자 네이밍 규칙은 어떤 것들이 있나요?</summary>
<div markdown="1">
별자는 특수문자를 제외한 문자, 숫자, 언더스코어(_), 달러 기호($)를 포함할 수 있습니다. <br/>
단 식별자는 특수문자를 제외한 문자, 언더스코어(_), 달러 기호로 시작해야 하며, 숫자로 시작하는 것은 허용하지 않습니다.
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
String, toString을 사용하여 문자열이 아닌 값을 문자열로 바꾸는 방법,  Number, parseInt를 사용해 숫자 타입으로 바꾸는 방법,  Boolen 메서드를 사용해서 불리언 타입으로 바꾸는 방법이 있습니다.
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
원본 배열을 직접 변경하는 push, pop, unshift, shift, splice, join, reverse, fill 등의 메소드와 새로운 배열을 생성하는 concat, slice, map, filter 등의 메소드가 있습니다.
</div>
</details>

<details>
<summary>고차 함수에 대해서 아나요?</summary>
<div markdown="1">
고차함수란 함수를 인수로 전달받거나(콜백함수) 함수를 반환하는 함수를 말합니다. sort, forEach, map, filter, reduce, some, every, find 등이 해당합니다.
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
<summary>
<script></script> 태그를 <body></body> 태그 밑에 둬야하는 이유가 있을까요? </summary>
<div markdown="1">
HTML 파서는 script 태그를 만나면 파싱을 멈추고 스크립트 파일을 읽기 때문에 HTML 코드 중간에 script 태그가 있으면 무거운 JavaScript 코드를 불러오고 실행하느라 DOM 생성이 지연됩니다.
DOM 생성이 지연되면 브라우저 렌더링에 방해가 되므로 미완성 화면이 오래 유지될 수 있습니다.
따라서 script 태그는 HTML 코드를 모두 작성 후 body 태그 닫기 직전에 작성하는 것이 좋습니다.
</div>
</details>

<br>

> DOM

<details>
<summary>DOM이 뭔가요?</summary>
<div markdown="1">
DOM은 HTML문서의 계층적 구조와 정보를 표현하며 이를 제어할 수 있는 API, 즉 프로퍼티와 메서드를 제공하는 트리 자료구조입니다.
</div>
</details>

<details>
<summary>DOM을 구성하는 건 뭐가 있나요? </summary>
<div markdown="1">
HTML 요소는 렌더링 엔진에 의해 파싱되어, DOM을 구성하는 요소 노드 객체로 변환됩니다. 이때 HTML 요소 어트리뷰트는 어트리뷰트 노드로, HTML 요소의 텍스트 콘텐츠는 텍스트 노드로 변환됩니다.
(문서 노드, 요소 노드, 어트리뷰트 노드, 텍스트 노드 등)
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
DOM 트리 상에 존재하는 모든 DOM 요소 노드에서 발생한 이벤트는 DOM 트리를 통해 전파됩니다.
이벤트가 전파되는 방향에 따라 3단계로 구분합니다.
캡처링 단계는 상위 요소에서 하위 요소 방향으로 전파되는 것,
타깃 단계는 이벤트가 이벤트 타깃에 도달하는 것,
버블링 단계는 하위 요소에 상위 요소 방향으로 전파되는 것입니다.
</div>
</details>

<details>
<summary>이벤트 위임(delegation)에 대해서 알고있나요?💥</summary>
<div markdown="1">
여러 개의 이벤트 리스너를 등록하지 않고 상위 요소에 하나의 이벤트 리스너만 등록하는 것을 이벤트 위임이라고 합니다. 여러개의 자식 엘리먼트 이벤트 관리하기,  동적 엘리먼트에 대한 이벤트 관리하기일 때 사용할 수 있습니다.
 <br> <br>
  <details>
  <summary>보충 설명</summary>

```jsx
이벤트위임을 사용하기 전
<ul>
  <li>1</li>
  <li>2</li>
  <li>3</li>
  <li>4</li>
  <li>5</li>
  <li>6</li>
</ul>

<script>
      const li = document.querySelectorAll("li");
      li.forEach((li) => {
        li.addEventListener("click", () => {
          li.classList.add("selected");
        });
      });
</script>
```

요소에 개별적으로 이벤트 리스너를 등록하고 있습니다. 이는 동일한 동작을 수행하는 요소에게 이벤트 리스너를 여러 번 중복해서 등록하는 것입니다. 여러개의 이벤트 리스너를 등록하는 경우, 각 요소에 대해 별도의 리스너를 등록하므로 메모리 사용량이 증가하고 많은 요소에 대한 이벤트 처리가 필요할 때 성능 저하가 일어날 수 있습니다. 또한 요소가 동적으로 추가 또는 제거되는 경우, 각각의 이벤트 리스너를 새로 등록하거나 제거해야하는 번거로움이 발생 할 수 있습니다.

```jsx
이벤트 위임을 사용한 예
      const ul = document.querySelector("ul");
      ul.addEventListener("click", (event) => {
        if (event.target.tagName == "LI") {
          event.target.classList.add("selected");
        }
      });
```

이벤트 위임을 사용한 예시는 상위 요소에 하나의 이벤트 리스너를 등록하여 모든 자식 요소의 이벤트를 처리합니다. 이벤트 위임을 사용하면 동적으로 생성되는 요소에 대해서도 이벤트 처리를 보장할 수 있으며, 이벤트 리스너의 중복 등록 문제를 피할 수 있습니다.

<div markdown="1">
</div>
  </details>
  
</div>
</details>

<details>
<summary>e.preventDefault에 대해 알고 있나요?</summary>
<div markdown="1">
e.preventDefault()는 메서드는 브라우저의 기본 동작을 중단시키는 역할을 합니다. 폼 제출 시 페이지를 새로고침하는 기본 동작을 중단시킵니다. 이를 통해 JavaScript 코드에서 추가적인 처리를 수행하거나 AJAX를 통해 비동기적으로 데이터를 전송할 수 있습니다.
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
프로토타입 기밥 객체 지향언어라서 다양한 객체 생성 방법을 지원합니다.<br>
- 객체 리터럴 `const obj = {}`<br>
- 생성자 함수<br>
- 클래스(ES6)<br>
- Object.create() 메서드<br>

  <br>
  <details>
  <summary>보충 설명</summary>
<div markdown="1">
  - 객체 리터럴 예시<br>
  
  ```jsx
const person = {
name: "John",
age: 30,
occupation: "Developer"
};
  ```
<br>
  - 생성자 함수 예시<br>
  
  ```jsx
//1번
function Person(name, age, occupation) {
  this.name = name;
  this.age = age;
  this.occupation = occupation;
}

const person = new Person("John", 30, "Developer");

//2번
var day = new Date(); // new 연산자를 사용하여 Date 타입의 객체를 생성함.
document.write("올해는 " + day.getFullYear() + "년입니다.");

````
<br>
- 클래스 예시<br>

 ``` jsx
class Person {
  constructor(name, age, occupation) {
    this.name = name;
    this.age = age;
    this.occupation = occupation;
  }
}

const person = new Person("John", 30, "Developer");
````

<br>
- Object.create() 메서드 예시<br>
  
  ```jsx
const personPrototype = {
  sayHello: function() {
    console.log("Hello!");
  }
};

const person = Object.create(personPrototype);
person.name = "John";
person.age = 30;
person.occupation = "Developer";

````



</div>
</details>


</div>
</details>

<br>

> 원시 값과 객체 비교

<details>
<summary>동적 타이핑을 지원하는 자바스크립트에서 데이터의 타입을 크게 2개로 나누는 이유가 있을까요?</summary>
<div markdown="1">
값은 메모리에 저장하고 참조할 수 있어야합니다. 메모리에 값을 저장하려면 확보해야 할 메모리 공간의 크기를 먼저 결정해야 합니다. 
첫째, 값을 저장할 때 확보할 메모리 공간의 크기를 결정하기 위해. 둘째, 값을 참조할 때 한번에 읽어 들여야 할 메모리 공간의 크기를 결정하기 위해. 셋째, 메모리에서 읽어 들인 2진수를 어떻게 해석할지 결정하기 위해.
</div>
</details>

<details>
<summary>값에 의한 전달이 뭔가요?💥</summary>
<div markdown="1">
값에 의한 전달은 원시 타입 메모리의 복사 방법입니다. 메모리에 저장된 값 100을 복사해서 다른 메모리 주소에 100(실제로는 2진수형태)을 저장하는 것을 말합니다.
</div>
</details>

<details>
<summary>참조에 의한 전달이 뭔가요?💥</summary>
<div markdown="1">
참조에 의한 전달은 객체 타입에서 복사하는 방법입니다. 메모리에 저장된 값이 아닌 100이 저장되어있는 메모리 주소를 복사해 다른 메모리에 저장되는 방식입니다.
</div>
</details>

<br>

> 함수

<details>
<summary>자바스크립트에서 함수를 정의하는 방법은 몇가지가 있나요?</summary>
<div markdown="1">
JavaScript에서 함수 정의하는 방식에는 함수 선언문, 함수 표현식, function 생성자 함수, 화살표함수(ES6) 등이 있습니다.
</div>
</details>

<details>
<summary>함수 선언문과 함수 표현식은 어떤 차이가 있나요? </summary>
<div markdown="1">
함수 선언문은 정의한 함수를 선언문 이전에 호출하면 함수 호이스팅에 의해 호출이 가능합니다. (undefined 출력)
var 키워드처럼 함수 스코프를 가져서 함수 안에서 선언된 함수는 밖에서 호출이 불가하고 if문과 같은 다른 코드 블록 안에서 선언된 함수는 전역처럼 접근 가능합니다.
  
함수 표현식은 함수 선언을 값처럼 사용하는 방식입니다. 함수 선언문과 달리 함수 표현식은 선언 이전에 접근이 불가하고 할당된 변수에 따라 스코프가 결정됩니다.
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
스코프에는 전역스코프와, 지역스코프가 있습니다. 전역 스코프(Global Scope)는 말 그대로 전역에 선언되어있어 어느 곳에서든지 해당 변수에 접근할 수 있다는 의미이며 지역 스코프(Local Scope)는 해당 지역에서만 접근할 수 있어 지역을 벗어난 곳에선 접근할 수 없다는 의미입니다. 지역스코프의 예로 함수스코프가 있습니다.
</div>
</details>

<details>
<summary>스코프에는 어떤 종류가 있죠?💥</summary>
<div markdown="1">
스코프에는 전역스코프와, 지역스코프가 있습니다. 전역 스코프(Global Scope)는 말 그대로 전역에 선언되어있어 어느 곳에서든지 해당 변수에 접근할 수 있다는 의미이며 지역 스코프(Local Scope)는 해당 지역에서만 접근할 수 있어 지역을 벗어난 곳에선 접근할 수 없다는 의미입니다. 지역스코프의 예로 함수스코프가 있습니다.
</div>
</details>

<details>
<summary>렉시컬 스코프를 아나요? 안다면 렉시컬 스코프는 무엇을 의미하나요?💥</summary>
<div markdown="1">
렉시컬 스코프란 함수를 어디서 정의했는지에 따라 함수의 상위 스코프를 결정하는 것을 말합니다. 즉, 함수의 상위 스코프는 항상 자신이 정의된 스코프가 되는 것입니다. JavaScript가 렉시컬 스코프를 따릅니다.
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
생성자 함수 통해 객체를 생성하면 마치 객체를 생성하기 위한 템플릿처럼 생성자 함수를 사용하여 프로퍼티 구조가 동일한 객체 여러개를 간편하게 생성할 수 있습니다.
</div>
</details>

<details>
<summary>생성자 함수가 객체(인스턴스)를 생성하는 과정에 대해 간략하게 설명해줄 수 있나요?</summary>
<div markdown="1">

```jsx
//1.생성자 함수 선언
function User(name) {
// this = { }  3. 빈 객체가 암시적으로 만들어짐

//4. 새로운 프로퍼티를 this에 추가함
[this.name](http://this.name/) = name;
this.isAdmin = false;

// return this; 5. this가 암시적으로 반환됨
}

let user = new User("쿠마") //2.인스턴스 생성
````

</div>
</details>

<br>

> 함수와 일급 객체

<details>
<summary>일급 객체가 뭔가요?</summary>
<div markdown="1">
일급 객체의 특징으로는
첫째, 무명의 리터럴로 생성할 수 있습니다.
둘째, 변수나 자료구조(배열,객체)에 저장할 수 있습니다.
셋째, 함수의 매개변수에 전달할 수 있습니다. (콜백함수)
넷째, 함수의 반환 값으로 사용할 수 있습니다. (고차함수)
</div>
</details>

<details>
<summary>자바스크립트에서 함수가 일급 객체라면, 일급 객체로 뭘 할 수 있나요?</summary>
<div markdown="1">
1. 변수에 할당할 수 있습니다: 함수는 변수에 할당되어 저장될 수 있습니다. 변수를 통해 함수를 참조하고 호출할 수 있습니다.<br><br>
2. 매개변수로 전달할 수 있습니다: 함수는 다른 함수의 매개변수로 전달될 수 있습니다. 이를 통해 함수를 콜백으로 사용하거나, 동적으로 함수를 생성하고 조작할 수 있습니다.<br><br>
3. 반환값으로 사용할 수 있습니다: 함수는 다른 함수의 반환값으로 사용될 수 있습니다. 이를 통해 함수가 다른 함수에 필요한 동작을 정의하고 반환하거나, 함수를 조합하여 더 복잡한 동작을 구성할 수 있습니다.<br><br>
이러한 특징을 통해 함수를 값처럼 다룰 수 있고, 함수를 조합하고 활용하여 유연하고 강력한 동작을 구현할 수 있습니다. 함수형 프로그래밍 패러다임에서는 이러한 특징을 기반으로 데이터와 동작을 분리하여 코드의 재사용성과 가독성을 높이는 등의 장점을 제공합니다.
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
순수 함수는 어떤 외부 상태에 의존하지도 않고, 변경하지도 않는, 즉 부수 효과가 없는 함수를 말합니다. 일반 함수는 외부 상태를 변경하는, 즉 부수 효과가 있는 함수를 말합니다.
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
객체지향 프로그래밍은 프로그램을 작은 독립적인 객체로 나누고, 이들을 상호작용시켜 큰 프로그램을 구축하는 개발 방법입니다. 레고 블록의 조립과 같이 필요한 기능을 수행하는 객체들을 조합하여 프로그램을 구성합니다. 객체들은 데이터와 그를 다루는 방법(메서드)을 포함하며, 이들은 상호작용하면서 프로그램이 실행됩니다. 객체지향 프로그래밍은 코드의 재사용성과 유지 보수의 편의성을 높여줍니다.
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
오타나 문법 지식의 미비로 인한 실수를 줄여 안정적인 코드를 생산하기 위해 ES5에 추가된 모드입니다.
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
개발자가 모든 기능을 구현하지 않고, 편하게 개발할 수 있도록 자바스크립트에서 기본적으로 제공하는 객체입니다.

Object, String, Number, Boolean, Symbol, Date, Math, RegExp, Array, Map/Set, WeakMap/WeakSet, Function, Promise, Reflect, Proxy, JSON, Error 등 40여개 표준 빌트인 객체가 있습니다.
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

<br>

> 타이머

<details>
<summary>타이머 함수에는 어떤 것들이 있나요?</summary>
<div markdown="1">
특정 함수의 실행을 원하는 시간만큼 뒤로 미루는 setTimeout, 특정 콜백을 일정한 시간 간격으로 반복 실행하도록 하는 setInterval이 있습니다. 각 타이머 취소하는 함수는 clearTimeout, clearInterval입니다.
</div>
</details>

<details>
<summary>이벤트가 과도하게 호출되어 성능에 문제를 일으킬 경우에 할 수 있는 어떤 일을 통해 해결할 수 있나요?</summary>
<div markdown="1">
짧은 시간 간격으로 연속해서 발생하는 scroll, resize, mousemove같은 이벤트에 바인딩한 이벤트 핸들러는 과도하게 호출되어 성능에 문제를 일으킬 수 있습니다.
디바운스와 쓰로틀과 같이 연이어 발생하는 이벤트를 그룹화해서 이벤트 핸들러의 호출을 방지하는 최적화 프로그래밍 기법을 사용하면 이벤트가 과도하게 호출되는 것을 막거나 조절할 수 있습니다.
</div>
</details>

<details>
<summary>디바운스에 대해서 알고 있나요?</summary>
<div markdown="1">
디바운스는 연이어 발생하는 이벤트를 그룹화해서, 맨 처음 혹은 마지막 함수만 호출되도록 하는 프로그래밍 기법입니다.
</div>
</details>

<details>
<summary>쓰로틀에 대해서 알고 있나요?</summary>
<div markdown="1">
쓰로틀은 연이어 발생하는 이벤트를 그룹화해서 일정한 delay를 포함시켜 일정 시간동안 호출된 함수는 무시하도록 하는 프로그래밍 기법입니다.
</div>
</details>

<br>

> 비동기 프로그래밍

<details>
<summary>동기와 비동기의 차이점에 대해서 설명해줄 수 있나요?</summary>
<div markdown="1">
동기는 현재 실행 중인 태스트가 종료될 때까지 다음에 실행될 태스크가 대기하는 방식이고 비동기는 현재 실행 중인 태스크가 종료되지 않은 상태라 해도 다음 태스크를 곧바로 실행하는 방식입니다. 비동기 방식에는 타이머 함수, HTTP 요청, 이벤트 핸들러 등이 있습니다.
</div>
</details>

<details>
<summary>이벤트 루프와 태스크 큐에 대해서 알고 있나요?</summary>
<div markdown="1">
이벤트루프는 순차적으로 태스크 큐에 대기 중인 함수를 콜 스택으로 이동, 즉 실행시키는 역할을 합니다. 태스크 큐는 비동기 함수의 콜백 함수 또는 이벤트 핸들러가 일시적으로 보관되는 영역입니다. 태스크 큐에 일시 보관된 함수들은 비동기 처리 방식으로 동작하는 것입니다.
</div>
</details>

<details>
<summary>마이크로태스크 큐에 대해서 알고 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>태스크 큐와 마이크로태스크 큐 중 어떤 것이 먼저 실행되나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> Ajax

<details>
<summary>JSON이 뭔가요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>JSON이 제공하는 정적 프로토타입 메서드에 대해 몇가지 말해볼 수 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>XMLHttpRequest와 fetch 메서드의 차이는 무엇이라고 생각하시나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> REST API

<details>
<summary>REST API가 뭔가요?</summary>
<div markdown="1">
REST API는 클라이언트와 서버 간의 통신을 위한 일련의 규칙과 제약을 정의한 소프트웨어 아키텍쳐 스타일입니다.
웹 브라우저, 모바일 앱과 같은 클라이언트에서 서버에게 요청을 보내고, 서버는 요청을 처리하고 필요한 데이터를 응답으로 반환하는 방식으로 동작합니다. 이러한 통신은 주로 HTTP 프로토콜을 사용하여 이루어집니다.
</div>
</details>

<details>
<summary>REST API의 구성은 어떤 것이 있나요?</summary>
<div markdown="1">
REST API는 리소스(자원)와 리소스를 조작하기 위한 표준 HTTP 메소드(GET, POST, PUT, DELETE 등)으로 구성되어 있습니다. 각각의 리소스는 고유한 식별자(URI)를 가지며, 클라이언트는 이 식별자를 사용하여 리소스에 접근하고 조작할 수 있습니다.
</div>
</details>

<details>
<summary>REST API를 설계하는데 중요한 것이 있을까요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>HTTP 요청 메서드에 대해서 아는대로 얘기해보세요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>HTTP 상태 코드를 아는대로 말해주세요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> Promise

<details>
<summary>콜백이란 뭐라고 생각하나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>프로미스가 뭔가요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>프로미스의 상태를 나타내는 것은 어떤 것들이 있나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>프로미스 빌트인 객체가 제공하는 정적 메서드에 대해 알고 있나요?</summary>
<div markdown="1">
프로미스 빌트인 객체가 제공하는 정적 메서드에는 여러 Promise 객체의 작업 성공 결과를 기다렸다가 모두 한 번에 취합하는 Promise.all 메서드, 여러 Promise 객체들을 경쟁시켜서 가장 빨리 상태가 결정된 Promise 객체를 선택하는 Promise.race 메서드, 배열 내 Promise 객체들이 settled 상태가 되기만 하면 Promise 객체를 리턴하는 Promise.allSettled 메서드 등이 있습니다. 
</div>
</details>

<br>

> 제너레이터와 async await

<details>
<summary>제너레이터란 뭔가요? 일반 함수와는 어떤 차이가 있죠?</summary>
<div markdown="1">
제너레이터는 코드블럭의 실행을 일시 중지(블러킹)했다가 필요한 시점에 재개할 수 있는 ES6에서 도입된 특수한 함수입니다.  
일반 함수와의 차이점은   
첫째, 함수 호출자에게 함수 실행의 제어권 양도가 가능한 것,  
둘째, 함수 호출자와 함수의 상태를 주고 받을 수 있는 것,  
호출 시 제너레이터 객체를 반환하는 것입니다.  
</div>
</details>

<details>
<summary>제너레이터의 구조</summary>
<div markdown="1">
제너레이터는 `yield` 키워드와 `next` 메서드를 통해 실행을 일시중지했다가 필요한 시점에 다시 재개할 수 있게 이루어져 있습니다. 
`next` 메서드를 통해 제너레이터를 실행할 경우, 코드 블록 내에 `yield` 키워드 뒤에 오는 표현식의 평가 결과를 제너레이터 함수 호출자에게 result 객체 형식으로 반환합니다.
</div>
</details>

<details>
<summary>Promise와 async/await의 차이점</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 에러

<details>
<summary>에러처리를 왜 해야 하나요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<details>
<summary>자바스크립트에서 에러를 처리하는 방법에는 뭐가 있을까요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>

<br>

> 모듈

<details>
<summary>모듈이 뭔가요?</summary>
<div markdown="1">
답변을 적어주세요
</div>
</details>




---
layout: single
title:  "24-03-21 5week 문제풀이"
---

## 첫번째문제 (준이)
```js
<body>
    <button onclick="quiz1()">
      C++과 자바는 클래스 기반 객체지향 언어이다.
    </button>
    <button onclick="quiz2()">프로퍼티는 객체의 상태를 나타내는 값이다.</button>
    <button onclick="quiz3()">
      자바스크립트 함수는 객체이고, 함수는 값으로 취급 가능하다.
    </button>

<script>
  function quiz1() {
            const answer= prompt('그렇다면 자바스크립트는 어떤  ***** ** **** 언어인가?');
          if(answer === '프로토타입 기반 객체지향'){
            alert("정답입니다~");
          }else
          alert("틀렸습니다.")
          };

          function quiz2() {
          const answer =  prompt('그렇다면 프로퍼티는 어떤 *와 *으로 구성되는가?');
          if(answer === '키, 값'){
              alert("정답입니다~");
          }else
          alert("틀렸습니다.")
          };

            function quiz3() {
            const answer = prompt ('이 말은 곧 ****값으로 사용 가능하다는 것이다.');
            if(answer === '프로퍼티'){
              alert("정답입니다~");
          }else
          alert("틀렸습니다.")
          };
 </script>
  </body>
```

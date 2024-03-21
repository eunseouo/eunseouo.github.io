---
layout: single
title:  "5week 메인문제풀이"
---

### 계산기 작동시키기- 미해결
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>계산기 작동시키기</title>
    <style>
      .calculator {
        display: flex;
        width: 400px;
        height: 230px;
        flex-direction: column;
        border: 1px solid black;
      }

      #display {
        display: flex;
        flex-direction: row;
        flex-basis: 30px;
        justify-content: end;
        line-height: 35px;
        margin: 5px;
        padding-right: 5px;
        background-color: rgb(223, 222, 222);
        border: 0.5px solid rgb(150, 153, 158);
      }
      .buttons {
        display: flex;
        justify-content: space-evenly;
        flex: 1 1 0;
      }
      button {
        width: 90px;
        height: 30px;
        margin: 1px;
        border: 0.5px solid rgb(150, 153, 158);
      }
      .zero {
        flex-basis: 190px;
        justify-content: space-evenly;
      }
      .equal {
        flex-direction: row;
        flex-basis: 385px;
      }

      [contenteditable]:empty:before {
        content: attr(placeholder);
      }
    </style>
  </head>
  <body>
    <div class="calculator">
      <div id="display" contenteditable placeholder="0"></div>
      <div class="buttons">
        <button onclick="number('9')">9</button>
        <button onclick="number('8')">8</button>
        <button onclick="number('7')">7</button>
        <button onclick="number('+')">+</button>
      </div>
      <div class="buttons">
        <button onclick="number('6')">6</button>
        <button onclick="number('5')">5</button>
        <button onclick="number('4')">4</button>
        <button onclick="number('-')">-</button>
      </div>
      <div class="buttons">
        <button onclick="number('3')">3</button>
        <button onclick="number('2')">2</button>
        <button onclick="number('1')">1</button>
        <button onclick="number('*')">*</button>
      </div>
      <div class="buttons">
        <button class="zero" onclick="number('0')">0</button>
        <button onclick="number('.')">.</button>
        <button onclick="number('/')">/</button>
      </div>
      <div class="buttons">
        <button class="equal" onclick="result()">=</button>
      </div>
    </div>
    <script>
      function number(a) {
        const num = document.getElementById('display');
        num.innerHTML += a;
      }

      function result() {
        var expression = document.getElementById('display').innerHTML;
        Number(expression);
      //console.log(expression);
        document.getElementById('display').innerHTML = expression;
      }
      //=계산이 안돼..!!!
    </script>
  </body>
</html>
```

나는 계산기 입력창에 문자열로 한꺼번에 넣었는데 <br>
그게 아니라 숫자+연산자+숫자 형식으로 입력되도록 해야한다..고 하셨음..<br>
이런!

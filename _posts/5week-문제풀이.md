---
layout: single
title:  "24-03-21 5week 문제풀이"
---

### 준이문제
```java
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
<br>
<br>

### 소정이문제
```java
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>소정이 문제</title>

    <style>
      .main {
        width: 400px;
        display: flex;
        justify-content: space-evenly;
      }
      .profil {
        text-align: center;
      }
      h1 {
        margin: 0px;
      }

      .box {
        width: 200px;
        height: 300px;
        border: 4px solid black;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
      }
      .name,
      .age,
      .hobby,
      .color {
        font-size: 30px;
        font-weight: 700;
        display: none;
      }
      .plus {
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
      }
      .minus {
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
      }
      button {
        width: 70px;
        height: 40px;
      }
      h2 {
        text-align: center;
        margin: 0;
      }
    </style>
  </head>
  <body>
    <div class="main">
      <div class="profil">
        <h1>프로필</h1>
        <div class="box">
          <div class="name">신은서</div>
          <div class="age">21살</div>
          <div class="hobby">뜨개질과 유튜브감상..^^</div>
          <div class="color">하늘색</div>
        </div>
      </div>

      <div class="plus">
        <h2>추가</h2>
        <button class="p_name">이름</button>
        <button class="p_age">나이</button>
        <button class="p_hobby">취미</button>
        <button class="p_color">색</button>
      </div>
      <div class="minus">
        <h2>삭제</h2>
        <button class="m_name">이름</button>
        <button class="m_age">나이</button>
        <button class="m_hobby">취미</button>
        <button class="m_color">색</button>
      </div>
    </div>

    <script>
      // 클릭하면 해당하는 값이 박스에 나오는 코드 
      const person = {};
      document.querySelector('.p_name').addEventListener('click', function p_btn_name() {
          person.name = 'eunseo';
          document.querySelector('.name').style.display = 'block';
          console.log(person);
        });
      document.querySelector('.p_age').addEventListener('click', function p_btn_age() {
          person.age = 21;
          document.querySelector('.age').style.display = 'block';
          console.log(person);
        });
      document.querySelector('.p_hobby').addEventListener('click', function p_btn_hobby() {
          person.hobby = '뜨개질과 유튜브감상..^^';
          document.querySelector('.hobby').style.display = 'block';
          console.log(person);
        });
      document.querySelector('.p_color').addEventListener('click', function p_btn_color() {
          person.color = '하늘색';
          document.querySelector('.color').style.display = 'block';
          console.log(person);
        });

        //클릭시 값 삭제되는 코드
        document.querySelector('.m_name').addEventListener('click', function m_btn_name() {
          document.querySelector('.name').style.display = 'none';
          delete person.name;
          console.log(person);
        });
        document.querySelector('.m_age').addEventListener('click', function m_btn_age() {
          document.querySelector('.age').style.display = 'none';
          delete person.age;
          console.log(person);
        });
        document.querySelector('.m_hobby').addEventListener('click', function m_btn_hobby() {
          document.querySelector('.hobby').style.display = 'none';
          delete person.hobby;
          console.log(person);
        });
        document.querySelector('.m_color').addEventListener('click', function m_btn_color() {
          document.querySelector('.color').style.display = 'none';
          delete person.color;
          console.log(person);
        });
    </script>
  </body>
</html>

```
<br>
<br>

### 윤아 문제
```java
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>윤아 문제</title>
    <style>
      body {
        font-family: Arial, sans-serif;
        background-color: lightgoldenrodyellow;
        margin: 0;
        padding: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 600px;
      }

      .container {
        text-align: center;
      }

      textarea {
        width: 300px;
        height: 200px;
        padding: 10px;
        margin-bottom: 10px;
        border-radius: 5px;
        border: 1px solid #ccc;
        resize: none;
        box-sizing: border-box;
      }

      button {
        background-color: #f8ff6c;
        color: rgb(27, 125, 0);
        border: none;
        padding: 10px 20px;
        border-radius: 5px;
        cursor: pointer;
        transition: background-color 0.2s;
      }

      button:hover {
        background-color: #eaff00;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <textarea id="memo" placeholder="메모를 입력하세요"></textarea>
      <br />
      <button onclick="saveMemo()">저장</button>
      <button onclick="clearMemo()">지우기</button>
    </div>

    <script>
      // 문제1.사용자가 입력한 메모를 가져와서 저장을 하면 메모가 저장되었다는 경고창을 표시함.
      function saveMemo() {
        const memo_str = document.getElementById('memo').value;
        alert('메모가 저장되었습니다.');
      }

      // 문제2. id가 memo인 입력 요소의 값을 빈 문자열로 설정하여 입력된 메모를 지웁니다.
      function clearMemo() {
        document.getElementById('memo').value = '';
      }
    </script>
  </body>
</html>

```
<br>
<br>

### 륜이 문제
```java
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <script>
      const student = {
        name: 'eunseo',
        age: 21,
        scores: {
          korean: 99,
          math: 70,
          english: 50,
        },
      };

      const sub1 = student.scores.korean;
      const sub2 = student.scores.math;
      const sub3 = student.scores.english;

      console.log(sub1 + sub2 + sub3);
      console.log((sub1 + sub2 + sub3) / 3);
    </script>
  </body>
</html>

```
<br>
<br>

### 예지 문제- 해결 못함
```java
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>객체 리터럴을 활용한 학생 정보</title>
  </head>
  <body>
    <div id="studentInfo"></div>

    <script>
      const students = [
        {
          이름: '전예지',
          나이: 21,
          정보: {
            키: 167,
            시력: -4.5,
          },
          좋아하는활동: ['영화시청', '쇼핑'],
          성별: '여성',
        },
        {
          이름: '장철수',
          나이: 24,
          정보: {
            키: 180,
            시력: 0.5,
          },
          좋아하는활동: ['축구', '댄스'],
          성별: '남성',
        },
        {
          이름: '김지민',
          나이: 18,
          정보: {
            키: 159,
            시력: -2.5,
          },
          좋아하는활동: ['미술', '독서'],
          성별: '여성',
        },
      ];

      const studentInfoContainer = document.getElementById('studentInfo');
      
      </script>
  </body>
</html>

```
<br>
<br>

### 보윤이 문제
```java
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>보윤이 문제</title>
    <style>
      .container {
        width: 400px;
        height: 500px;
        background-color: #dbddf9;
        padding: 10px;
        text-align: center;
      }

      input {
        text-align: center;
        width: 250px;
        height: 30px;
        font-size: 17px;
      }

      button {
        width: 50px;
        height: 33px;
      }

      #list {
        text-align: left;
        font-size: 17px;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <h1>오늘의 할 일</h1>
      <input
        type="text"
        id="inputList"
        placeholder="오늘의 할 일을 입력하세요"
      />
      <button onclick="addList()">추가</button>
      <ul id="list"></ul>
    </div>

    <script>
      const toDoList = document.querySelector('#list');


      function addList() {
        // addList() : 사용자가 입력한 일을 가져와서 리스트에 추가하는 함수
        // trim()을 사용하여 입력한 문자열 앞뒤의 공백 제거하여 문자열의 내용만 남기기--해결 못함
        const userInput = document.getElementById('inputList').value;

        
          // 문자열이 비어있지 않는다면3
          if (userInput != '') {
             // 리스트의 내용을 출력하기 위해 빈 ul 요소를 만들어주고
            const newList = document.createElement('ul');
            newList.textContent = userInput;
        
          // appendChild()를 사용하여 ul 요소의 문자열을 리스트에 추가해준 후
            document.getElementById('list').appendChild(newList);
        
            // 입력 필드 비우기
            document.getElementById('inputList').value = '';
          
              
          }else {
            // 문자열이 공백이라면 입력하라는 알림 띄우기
            alert('값을 입력하세요.');
          };

        }
    </script>
  </body>
</html>

```

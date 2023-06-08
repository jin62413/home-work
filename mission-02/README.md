# 🧩Mission - 02
position과 float를 활용하여 webCafe의 로그인 화면 구현
<br><br>

## ✔ 완성된 UI

![완성본](./login-form.PNG "완성본 스크린샷")
<br><br>

## ✔ 설명

__HTML 구조__

<img src="./login_structure.jpg" width="450px" alt="structure image" />

* content-container로 모든 컨텐츠 감싸기
* header로 제목 추가
* login-form-container로 모든 요소 감싸기
* login-group로 아이디/비밀번호 입력창, 로그인 버튼 묶기
* login-id-password-wrapping으로 아이디/비밀번호 input 묶기
* member-service로 회원가입, 아이디 비밀번호 찾기 묶기
<br><br>

__CSS 코드__

* form 태그를 사용하여 로그인 기능 구현
* box-shadow를 사용해 content-container에 그림자 생성
  ```CSS
  .content-container {
    box-shadow: 4px 4px #a3a3a3;
  }
  ```
* legend 태그의 내용은 숨김 처리
  ```CSS
  .a11y {
    overflow: hidden;
    position: absolute !important;
    clip: rect(0, 0, 0, 0);
    clip-path: inset(50%);
    width: 1px;
    height: 1px;
    margin: -1px;
  }
  ```
* fieldset 태그로 생기는 border 없애기
  ```CSS
  fieldset {
    border: 0;
  }
  ```
* login-group 내의 button 요소는 position을 사용하여 정렬
  ```CSS
  .login-form-container {
    position: relative;
  }

  .login__btn {
    position: absolute;
    top: 8px;
    right: 8px;
  }
  ```
* login-group에서 border-bottom으로 밑줄 효과 주기
  ```CSS
  .login-group {
    border-bottom: 1px solid #CCCCCC;
  }
  ```
* login-id-password-wrapping 내의 label과 input 요소도 position을 사용하여 정렬
  ```CSS
  .login-id-password-wrapping {
    position: relative;
  }

  .login-id-password-wrapping label{
    position: absolute;
    left: 0;
  }

  .login-id-password-wrapping input {
    position: absolute;
    right: 0;
  }
  ```
* member-service 내의 span 요소는 float를 사용하여 정렬
  ```CSS
  .member__join {
    float: left;
    line-height: 28px;
  }

  .member__search {
    float: right;
    line-height: 28px;
  }
  ```
* ::before를 사용해 span 앞쪽에 꺽쇠 삽입, 박스 위쪽과 오른쪽에 border를 주고 45도 회전시켜 꺽쇠 만들기
  ```CSS
  .member__join::before,
  .member__search::before {
    content: "";
    border-top: 3px solid #ED552F;
    border-right: 3px solid #ED552F;
    width: 5px;
    height: 5px;
    display: inline-block;
    transform: rotate(45deg);
  }
  ```
<br>

## ✔ 아쉬운 점

* div를 너무 많이 사용한 것 같다.
* width 값을 div마다 줬는데 비효율적인 느낌이어서 다음에는 더 효율적인 방법을 찾고싶다.
* README를 이렇게 쓰는게 맞는지 모르겠다.
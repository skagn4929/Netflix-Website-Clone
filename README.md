# Netflix-Website-Clone
**HTML과 CSS를 사용하여 넷플릭스 웹사이트 클론을 만들어 보았습니다.**
- https://skagn4929.github.io/Netflix-Website-Clone/

![넷플릭스 클론 완성본](https://github.com/skagn4929/Netflix-Website-Clone/assets/134206709/37f650e6-aff2-49d0-9bd7-0d39996b7a4a)

---

## 1. 프로젝트의 동기   
**클론 코딩을 통한 HTML 과 CSS 언어의 학습**

## 2. 프로젝트 주요 내용   
**1. 헤더섹션에 넷플릭스 로고를 넣고 언어선택 및 회원가입 버튼을 만들었습니다.**

![넷플1](https://github.com/skagn4929/Netflix-Website-Clone/assets/134206709/f75e59f7-b72a-45f7-bfce-434fada2a7cd)

- HTML
```html
<div class="header">
  <nav>
    <img src="images/logo.png" class="logo" />
    <div>
      <button class="language-btn">
      English <img src="images/down-icon.png" />
      </button>
      <button>Sign In</button>
    </div>
  </nav>
</div>
```
- CSS
```css
nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px 0;
}

.logo {
  width: 150px;
  cursor: pointer;
}
nav button {
  border: 0;
  outline: 0;
  background: #db0001;
  color: #fff;
  padding: 7px 20px;
  font-size: 12px;
  border-radius: 4px;
  margin-left: 10px;
  cursor: pointer;
}

.language-btn {
  display: inline-flex;
  align-items: center;
  background: transparent;
  border: 1px solid #fff;
  padding: 7px 10px;
}
.language-btn img {
  width: 10px;
  margin-left: 10px;
}
```

---

**2. 헤더섹션 중앙에 환영 텍스트와 이메일 구독 양식을 만들었습니다.**

![넷플2](https://github.com/skagn4929/Netflix-Website-Clone/assets/134206709/1c87a75e-1fa7-40b9-aa31-41be8f43a6b0)

- HTML
```html
<div class="header-content">
  <h1>Unlimited movies, TV shows, and more</h1>
  <h3>Watch anywhere. Cancel anytime.</h3>
  <p>
    Ready to watch? Enter your email to create or restart your membership.
  </p>
  <form class="email-signup">
    <input type="email" placeholder="Email address" required />
    <button type="submit">Get Started</button>
  </form>
</div>
```
- CSS
```css
.header-content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  margin-top: 100px;
}
.header-content h1 {
  font-size: 60px;
  line-height: 70px;
  font-weight: 600;
  max-width: 650px;
}
.header-content h3 {
  font-weight: 400;
  margin-bottom: 20px;
}
.email-signup {
  background: #fff;
  border-radius: 4px;
  display: flex;
  align-items: center;
  margin-top: 30px;
  overflow: hidden;
}
.email-signup input {
  flex: 1;
  border: 0;
  outline: 0;
  margin-left: 20px;
}
.email-signup button {
  background: #db0001;
  border: 0;
  outline: 0;
  color: #fff;
  font-size: 16px;
  cursor: pointer;
  padding: 15px 30px;
}
```

---

**3. 본문 하단에 FAQ를 만들어 + 버튼 클릭 시 세부사항이 표시되게 만들었습니다.**

https://github.com/skagn4929/Netflix-Website-Clone/assets/134206709/e03603c2-c99d-43e8-bd82-ef7f918a20cf

- HTML
```html
<div class="faq">
    <h2>Frequently Asked Questions</h2>
    <ul class="accordion">
      <li>
        <input type="radio" name="accordion" id="first" />
        <label for="first">What is Netflix?</label>
        <div class="content">
          <p>
            Netflix is a streaming service that offers a wide variety of
            award-winning TV shows, movies, anime, documentaries, and more on
            thousands of internet-connected devices. You can watch as much as
            you want, whenever you want - all for one low monthly price.
            There's always something new to discover and new TV shows and
            movies are added every week!
          </p>
        </div>
      </li>
      <li>...생략...</li>
      <li>...생략...</li>
      <li>...생략...</li>
      <li>...생략...</li>
      <li>...생략...</li>
    </ul>  
```
- CSS
```css
.faq {
  padding: 10px 12%;
  text-align: center;
  font-size: 18px;
}
.faq h2 {
  font-weight: 500;
  font-size: 40px;
}

.accordion {
  margin: 60px auto;
  width: 100%;
  max-width: 750px;
}

.accordion li {
  list-style: none;
  width: 100%;
  padding: 5px;
}

.accordion li label {
  display: flex;
  align-items: center;
  padding: 20px;
  font-size: 18px;
  font-weight: 500;
  background: #303030;
  margin-bottom: 2px;
  cursor: pointer;
  position: relative;
}
label::after {
  content: "+";
  font-size: 34px;
  position: absolute;
  right: 20px;
  transition: transform 0.5s;
}
input[type="radio"] {
  display: none;
}
.accordion .content {
  background: #303030;
  text-align: left;
  padding: 0 20px;
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.5s, padding 0.5s;
}
.accordion input[type="radio"]:checked + label + .content {
  max-height: 600px;
  padding: 30px 20px;
}
.accordion input[type="radio"]:checked + label::after {
  transform: rotate(135deg);
}
```

---

### 이미지 참고
- www.netflix.com











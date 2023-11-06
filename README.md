# social-media-selector-menu

<img src="./social%20media%20selector%20menu.gif" style="width:400px">  

## 기능    
메뉴를 클릭하면, 소셜미디어 아이콘으로 이동하는 메뉴 

<br>

## 사용한 라이브러리
**fontawesome**     
https://fontawesome.com/

<br>

## 학습  
### 1. css : visibility  
: <u>문서의 레이아웃을 변경하지 않고 요소를 보이거나 숨기기</u>  
: 만약에 문서를 숨기고, 레이아웃에서도 제외를 하려면 <u>`<display:none>`</u> 설정  
: 속성값 

|속성값|의미|
|---|---|
|visible|요소가 보임|
|hidden|요소가 숨겨짐(그려지지 않음). 레이아웃에는 숨겨지지 않았을 때와 동일한 영향|
|collapse|내부 테이블 객체(행, 행 그룹, 열 및 열 그룹)에 적용된다. hidden과 유사

### 2. js : toggle  
: on/off 스위치 개념으로 스위치를 켰다 껐다 하는 기능을 가지고 있음    
: add()와 remove() 메서드를 한번에 쓸 수 있는 합쳐진 개념  
: 보통 click 이벤트에 classList를 이용하여 toggle로 css style을 준 클래스를 on/off 처리함 


### 3. js : forEach
: 배열 순환 메서드  
: for문과 다른점은, forEach 메서드는 매개변수(parameter)와 함께 배열의 각 요소에 적용하게 될 콜백 함수(callback function)를 전달
|매개변수|의미|
|---|---|
|Current Value (명명된 매개변수) | 처리할 현재 요소
|Index (선택적 매개변수) | 처리할 현재 요소의 인덱스
|Array (선택적 매개변수) | forEach 메서드를 호출한 배열


### 4. 코드 이해
```
const menuEl = document.querySelector(".menu");
const menuTextEl = document.querySelector(".menu p");
const socialListsEl = document.querySelector(".social-lists");
const liEls = document.querySelectorAll(".social-lists li");

menuEl.addEventListener("click", () => {
  socialListsEl.classList.toggle("hide");
  menuEl.classList.toggle("rotate");
});

```

: menuEl(메뉴)를 클릭을 하면, <br>
socialListsEl(ul)에 클래스 hide가 toggle 이벤트가 적용이 되어 스위치를 on 한 것처럼 보임 (visibility: visible;). 
<br> + menuEl(메뉴)의 rotate 클래스에 toggle 이벤트를 적용 

<br>  

```
liEls.forEach(liEl => {
  liEl.addEventListener("click", ()=> {
    menuTextEl.innerHTML = liEl.innerHTML;
    socialListsEl.classList.remove("hide");
    menuEl.classList.toggle("rotate");
  });
});
```
: liEls(li요소들) 배열은 순환시, 각 liEl(li요소)를 클릭을 하면, <br> menuTextEl(p태그)에 liEl.innerHTML을 삽입
<br> + socialListsEl(ul태그)에 클래스 hide를 삭제 <br> +
menuEl(menu)에 클래스 rotate에 toggle 이벤트를 적용

<br>

## 학습 출처  

<br>

**유튜브**  
https://www.youtube.com/@JavaScriptKing  

**js : toggle**   
https://goddino.tistory.com/129

**css**  
https://developer.mozilla.org/  
https://www.w3schools.com/  

**js : forEach**  
https://www.freecodecamp.org/korean/news/javascript-foreach-how-to-loop-through-an-array/  

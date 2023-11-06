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
### 1. js : toggle  
: on/off 스위치 개념으로 스위치를 켰다 껐다 하는 기능을 가지고 있음    
: add()와 remove() 메서드를 한번에 쓸 수 있는 합쳐진 개념  
: 보통 click 이벤트에 classList를 이용하여 toggle로 css style을 준 클래스를 on/off 처리함 

```
menuEl.addEventListener("click", () => {
  socialListsEl.classList.toggle("hide");
  menuEl.classList.toggle("rotate");
});
```


<br>

## 학습 출처  

<br>

**유튜브**  
https://www.youtube.com/@JavaScriptKing  

**js : toggle**   
https://goddino.tistory.com/129
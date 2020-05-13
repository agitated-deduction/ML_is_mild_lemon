# colab 런타임 연결 끊김 방지 코드

```js
function ClickConnect() { 
// 백엔드를 할당하지 못했습니다. 
// GPU이(가) 있는 백엔드를 사용할 수 없습니다. 가속기가 없는 런타임을 사용하시겠습니까? 
// 취소 버튼을 찾아서 클릭 
  var buttons = document.querySelectorAll("colab-dialog.yes-no-dialog paper-button#cancel"); 
  buttons.forEach(function(btn) { 
    btn.click(); 
  }); 
  console.log("1분마다 자동 재연결"); 
  document.querySelector("#top-toolbar > colab-connect-button").click(); 
} 
setInterval(ClickConnect,1000*60);

```
<br>

```js
function CleanCurrentOutput(){ 
  var btn = document.querySelector(".output-icon.clear_outputs_enabled.output-icon-selected[title$='현재 실행 중...'] iron-icon[command=clear-focused-or-selected-outputs]");
  if(btn) { 
    console.log("30분마다 출력 지우기"); 
    btn.click(); 
  } 
}
setInterval(CleanCurrentOutput,1000*60*30);
```

출처: https://bryan7.tistory.com/1077 [민서네집]

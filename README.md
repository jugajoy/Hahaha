<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,
initial-scale=1.0">
<link rel="stylesheet" href="(f url_for (static,
filename='style.css") ))">
<title>심심이와 대화하기</title>
</head>
<body>
<div class="chat-container">
<h1>심심이와 대화하기</h1>
<div id="chat-box"></div>
<input type="text" id="user-input
placeholder="메시지를 입력하세 요...">
<button id="send-button"> </button>
</div>


<script>
document.getElementByld('send-bu
tton).addEventListener("click', function(


const userlnput
document.getElementByld('user-input").value;
const chatBox
document.getElementByld(chat-box);


1 사용자 메시지 추가
chatBox.innerHTML +=


<div>사용자: $(userlnput)</


div>`;


1 서버에 요청
fetch(/chat',
method: 'POST
headers:
Content-Type': 'application/json


body: JSON. stringify(f message: userlnput ))
-


then(response => response.json())
then(data =>(
1| 심심이 메시지 추가
chatBox.innerHTML += `<div>심심이: $
fdata.response</div>;
document.getElementByld('user-input"). value =
</script>
</body>
</html>

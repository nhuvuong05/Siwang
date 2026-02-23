<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<title>Chúc mừng sinh nhật bé Chan</title>

<style>

*{box-sizing:border-box}

body{
margin:0;
font-family:-apple-system,BlinkMacSystemFont,system-ui,Roboto;
background:linear-gradient(135deg,#ff9a9e,#fad0c4);
min-height:100vh;
display:flex;
justify-content:center;
align-items:center;
padding:20px;
overflow:hidden;
}

/* ===== FORM NHẬP PASS ===== */

.box{
width:100%;
max-width:360px;
background:white;
padding:28px 22px;
border-radius:22px;
text-align:center;
box-shadow:0 15px 35px rgba(0,0,0,.18);
animation:fade .6s ease;
}

@keyframes fade{
from{opacity:0;transform:translateY(20px)}
to{opacity:1}
}

h3{
margin-top:0;
font-size:20px;
}

input{
width:100%;
padding:16px;
font-size:20px;
border-radius:14px;
border:1px solid #ddd;
text-align:center;
margin-top:8px;
outline:none;
}

input:focus{
border:1px solid #ff4d6d;
}

button{
width:100%;
margin-top:16px;
padding:16px;
border:none;
border-radius:16px;
background:#ff4d6d;
color:white;
font-size:18px;
font-weight:600;
}

.fadeText{
margin-top:12px;
font-size:14px;
color:#888;
opacity:.5;
display:none;
}

/* ===== LÁ THƯ ===== */

.envelope{
display:none;
position:fixed;
left:50%;
top:50%;
transform:translate(-50%,-50%);
width:92%;
max-width:420px;
max-height:80vh;
overflow:auto;
background:white;
padding:28px 22px;
border-radius:24px;
box-shadow:0 20px 45px rgba(0,0,0,.25);
text-align:center;
animation:open .7s ease;
}

@keyframes open{
from{transform:translate(-50%,-40%) scale(.7);opacity:0}
to{transform:translate(-50%,-50%) scale(1);opacity:1}
}

.envelope p{
line-height:1.6;
font-size:17px;
}

h2{color:#ff4d6d}

/* ===== TIM BAY ===== */

.hearts{
position:fixed;
bottom:-20px;
font-size:22px;
animation:fly 4s linear forwards;
}

@keyframes fly{
to{
transform:translateY(-110vh);
opacity:0;
}
}

</style>
</head>

<body>

<div class="box" id="loginBox">
<h3>🔐 Nhập mật mã để mở thư</h3>
<input id="pass" type="password" placeholder="Nhập 6 số">
<button onclick="check()">Mở thư 💌</button>
<div class="fadeText" id="wrong">Sinh nhật người đặc biệt 💫</div>
</div>

<div class="envelope" id="letter">

<h2>🎂 Chúc mừng sinh nhật bé Chan 🎂</h2>

<p>
Chúc <b>Quách Thị Thu Trang</b> (24/02/2004)  
một tuổi mới thật nhiều niềm vui, hạnh phúc  
và luôn xinh đẹp rạng rỡ 💖
</p>

<p>
Cảm ơn em vì đã đến bên anh,  
làm cuộc sống của anh ấm áp và ý nghĩa hơn mỗi ngày 🌹
</p>

<p>
Hy vọng mọi sinh nhật sau này  
anh vẫn luôn được ở cạnh em,  
chúc em cười thật nhiều, hạnh phúc thật lâu ✨
</p>

<p><i>Người tạo: Nguyễn Như Vương</i></p>

</div>

<script>

function check(){
let p=document.getElementById("pass").value.trim();
let wrong=document.getElementById("wrong");

if(p==="240204"){

document.getElementById("loginBox").style.display="none";
document.getElementById("letter").style.display="block";

/* tim bay */
for(let i=0;i<30;i++){
let h=document.createElement("div");
h.className="hearts";
h.innerHTML="💖";
h.style.left=Math.random()*100+"vw";
h.style.animationDelay=Math.random()*2+"s";
document.body.appendChild(h);
}

}else{
wrong.style.display="block";
}

}

document.getElementById("pass").addEventListener("keydown",e=>{
if(e.key==="Enter") check();
});

</script>

</body>
</html>

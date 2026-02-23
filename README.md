<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Chúc mừng sinh nhật bé Chan</title>

<style>

/* RESET */
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto;
}

html,body{
height:100%;
}

/* NỀN HỒNG + CĂN GIỮA */
body{
min-height:100dvh;
display:flex;
justify-content:center;
align-items:center;
background:linear-gradient(135deg,#ff9a9e,#fad0c4);
padding:20px;
position:relative;
overflow-x:hidden;
}

/* ===== FORM LOGIN ===== */

.box{
width:100%;
max-width:420px;
background:white;
padding:32px 24px;
border-radius:26px;
text-align:center;
box-shadow:0 20px 50px rgba(0,0,0,.25);
margin:auto;                /* QUAN TRỌNG: giữ giữa */
}

h3{
font-size:clamp(18px,4vw,22px);
margin-bottom:14px;
}

input{
width:100%;
padding:16px;
font-size:clamp(16px,4vw,20px);
border-radius:14px;
border:1px solid #ddd;
text-align:center;
}

button{
width:100%;
margin-top:16px;
padding:16px;
border:none;
border-radius:16px;
background:#ff4d6d;
color:white;
font-size:clamp(16px,4vw,18px);
font-weight:600;
cursor:pointer;
}

.fadeText{
margin-top:12px;
font-size:14px;
opacity:.6;
display:none;
}

/* ===== THIỆP ===== */

.envelope{
display:none;

/* CĂN GIỮA CHUẨN MỌI MÀN HÌNH */
position:fixed;
inset:0;
margin:auto;

width:min(92vw,520px);
max-height:85dvh;
overflow:auto;

background:white;
padding:34px 26px;
border-radius:28px;
text-align:center;
box-shadow:0 30px 70px rgba(0,0,0,.3);

animation:open .6s ease;
}

/* animation mở */
@keyframes open{
from{
opacity:0;
transform:scale(.85);
}
to{
opacity:1;
transform:scale(1);
}
}

.envelope p{
font-size:clamp(16px,4vw,18px);
line-height:1.65;
margin:12px 0;
}

h2{
color:#ff4d6d;
font-size:clamp(22px,5vw,28px);
margin-bottom:6px;
}

/* ===== TIM BAY ===== */

.hearts{
position:fixed;
bottom:-20px;
font-size:22px;
animation:fly 4s linear forwards;
pointer-events:none;
}

@keyframes fly{
to{
transform:translateY(-120vh);
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

<div class="fadeText" id="wrong">
Sinh nhật người đặc biệt 💫
</div>
</div>

<div class="envelope" id="letter">

<h2>🎂 Chúc mừng sinh nhật bé Chan 🎂</h2>

<p>
Chúc bé <b>Quách Thị Thu Trang</b> (24/02/2026)  
một tuổi mới thật nhiều niềm vui, hạnh phúc  
và luôn xinh đẹp 💖
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

document.getElementById("wrong").style.display="block";

}

}

document.getElementById("pass").addEventListener("keydown",e=>{
if(e.key==="Enter") check();
});

</script>

</body>
</html>

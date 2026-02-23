<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Chúc mừng sinh nhật bé Chan</title>

<style>
body{
margin:0;
font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto;
background:linear-gradient(135deg,#ff9a9e,#fad0c4);
height:100vh;
display:flex;
justify-content:center;
align-items:center;
overflow:hidden;
}

/* hộp nhập mật khẩu */
.box{
background:white;
padding:30px;
border-radius:20px;
text-align:center;
box-shadow:0 10px 30px rgba(0,0,0,0.2);
}

input{
padding:12px;
font-size:18px;
border-radius:10px;
border:1px solid #ddd;
text-align:center;
width:160px;
}

button{
margin-top:15px;
padding:12px 20px;
border:none;
border-radius:12px;
background:#ff4d6d;
color:white;
font-size:16px;
}

.fadeText{
margin-top:15px;
color:#999;
opacity:0.45;
display:none;
}

/* phong thư */
.envelope{
display:none;
position:absolute;
width:90%;
max-width:420px;
background:white;
padding:25px;
border-radius:20px;
box-shadow:0 15px 40px rgba(0,0,0,0.25);
text-align:center;
animation:zoom .6s ease;
}

@keyframes zoom{
from{transform:scale(.5);opacity:0}
to{transform:scale(1);opacity:1}
}

h2{color:#ff4d6d}

/* tim bay */
.hearts{
position:absolute;
font-size:22px;
animation:fly 3s linear infinite;
}

@keyframes fly{
from{transform:translateY(0);opacity:1}
to{transform:translateY(-600px);opacity:0}
}
</style>
</head>

<body>

<div class="box" id="loginBox">
<h3>🔐 Nhập mật mã để mở thư</h3>
<input id="pass" type="password" placeholder="6 số">
<br>
<button onclick="check()">Mở thư 💌</button>
<div class="fadeText" id="wrong">sinh nhật người đặc biệt</div>
</div>

<div class="envelope" id="letter">
<h2>🎂 Chúc mừng sinh nhật bé Chan 🎂</h2>

<p><b>Quách Thị Thu Trang</b><br>
Sinh ngày 24/02/2004 💖</p>

<p>
Chúc em tuổi mới luôn vui vẻ, hạnh phúc,  
xinh đẹp và gặp thật nhiều may mắn trong cuộc sống 🌸
</p>

<p>
Cảm ơn em vì đã xuất hiện trong cuộc đời anh,  
làm mọi ngày của anh trở nên ý nghĩa hơn ✨
</p>

<p>
Hy vọng những sinh nhật sau này  
anh vẫn luôn được ở cạnh em 💞
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
for(let i=0;i<25;i++){
let h=document.createElement("div");
h.className="hearts";
h.innerHTML="💖";
h.style.left=Math.random()*100+"%";
h.style.top="80%";
h.style.animationDelay=Math.random()*2+"s";
document.body.appendChild(h);
}

}else{
wrong.style.display="block";
}
}

/* Enter để mở */
document.getElementById("pass").addEventListener("keydown",function(e){
if(e.key==="Enter") check();
});
</script>

</body>
</html>

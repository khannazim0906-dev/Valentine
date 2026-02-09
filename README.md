<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Valentine ❤️</title>

<style>
body {
  margin: 0;
  height: 100vh;
  background: linear-gradient(135deg, #ffdde1, #ee9ca7);
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: Arial, sans-serif;
}

.container {
  text-align: center;
}

h1 {
  color: #b3003b;
  font-size: 38px;
  margin-bottom: 30px;
}

button {
  padding: 15px 30px;
  font-size: 22px;
  border: none;
  border-radius: 10px;
  cursor: pointer;
}

#yes {
  background: #ff4d6d;
  color: white;
}

#no {
  background: white;
  margin-left: 20px;
  position: absolute;
}
</style>
</head>

<body>

<div class="container">
  <h1>Will you be my Valentine? 💖</h1>
  <button id="yes" onclick="goYes()">YES 😍</button>
  <button id="no">NO 🙄</button>
</div>

<script>
const noBtn = document.getElementById("no");
const yesBtn = document.getElementById("yes");
let size = 22;

noBtn.addEventListener("mouseover", moveNo);
noBtn.addEventListener("click", moveNo);

function moveNo() {
  const x = Math.random() * (window.innerWidth - 120);
  const y = Math.random() * (window.innerHeight - 60);
  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";

  size += 4;
  yesBtn.style.fontSize = size + "px";
}

function goYes() {
  window.location.href = "memories.html";
}
</script>

</body>
</html>

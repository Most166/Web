<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>กำลังโหลดรูป...</title>

<style>
body {
  margin: 0;
  height: 100vh;
  background: #f2f2f2;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: system-ui, sans-serif;
}

.card {
  background: #fff;
  padding: 30px;
  border-radius: 16px;
  box-shadow: 0 10px 30px rgba(0,0,0,.15);
  text-align: center;
  width: 90%;
  max-width: 360px;
}

h2 {
  margin-bottom: 10px;
}

p {
  color: #666;
  font-size: 14px;
}

button {
  margin-top: 20px;
  width: 100%;
  padding: 16px;
  font-size: 18px;
  border: none;
  border-radius: 12px;
  background: #007aff;
  color: #fff;
  cursor: pointer;
}

button:active {
  transform: scale(0.98);
}
</style>
</head>

<body>

<div class="card">
  <h2>📸 รูปนี้ถูกเบลอ</h2>
  <p>กดยืนยันเพื่อดูรูปแบบชัด</p>
  <button id="btn">ดูรูป</button>
</div>

<audio id="sound" preload="auto">
  <source src="new-meme-53393.mp3" type="audio/mpeg">
</audio>

<script>
document.getElementById("btn").addEventListener("click", () => {
  const audio = document.getElementById("sound");
  audio.volume = 1.0;
  audio.currentTime = 0;
  audio.play();

  if (navigator.vibrate) {
    navigator.vibrate([200,100,200,100,400]);
  }

  document.querySelector(".card").innerHTML = "<h2>❌ โหลดไม่สำเร็จ</h2><p>กรุณาลองใหม่ภายหลัง</p>";
});
</script>

</body>
</html>

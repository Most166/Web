
<html lang="th">
<head>
<meta charset="UTF-8">
<title>ดูรูป</title>
</head>
<body style="text-align:center; margin-top:100px;">

<h2>📸 กดเพื่อดูรูป</h2>
<button id="btn" style="font-size:30px;">กดเลย</button>

<audio id="sound" preload="auto">
  <source src="new-meme-53393.mp3" type="audio/mpeg">
</audio>

<script>
document.getElementById("btn").addEventListener("click", () => {
  const audio = document.getElementById("sound");
  audio.volume = 1.0;
  audio.currentTime = 0;
  audio.play().catch(e => alert("ไม่สามารถเล่นเสียงได้"));
});
</script>


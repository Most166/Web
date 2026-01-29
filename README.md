<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<title>ดูรูป</title>
</head>
<body style="text-align:center; margin-top:100px;">

<h2>📸 กดเพื่อดูรูป</h2>
<button onclick="boom()" style="font-size:30px;">กดเลย</button>

<audio id="sound" src="new-meme-53393.mp3"></audio>

<script>
function boom() {
  const audio = document.getElementById("sound");
  audio.volume = 1.0;
  audio.play();
}
</script>

</body>
</html>

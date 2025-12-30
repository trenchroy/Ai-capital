# Ai-capital
Auto caption generator 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Auto Caption Video</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body{
  margin:0;
  font-family:Arial, sans-serif;
  background:#0b0b0b;
  color:#fff;
}
.container{
  max-width:600px;
  margin:auto;
  padding:20px;
}
h1{
  text-align:center;
  color:#00ffcc;
}
.card{
  background:#151515;
  padding:20px;
  border-radius:8px;
}
input[type=file]{
  width:100%;
  padding:10px;
  background:#000;
  color:#fff;
  border:1px solid #333;
}
button{
  width:100%;
  margin-top:12px;
  padding:12px;
  background:#00ffcc;
  border:none;
  font-size:16px;
  cursor:pointer;
}
button:disabled{
  background:#555;
}
#status{
  margin-top:10px;
  font-size:14px;
}
#captions{
  margin-top:15px;
  background:#000;
  padding:10px;
  height:200px;
  overflow:auto;
  border:1px solid #333;
  white-space:pre-line;
}
.footer{
  text-align:center;
  margin-top:15px;
  font-size:12px;
  color:#777;
}
</style>
</head>

<body>
<div class="container">
  <h1>Auto Caption Video</h1>

  <div class="card">
    <input type="file" id="videoInput" accept="video/*">
    <button id="genBtn" onclick="generateCaptions()">Generate Captions</button>
    <div id="status"></div>
    <div id="captions"></div>
  </div>

  <div class="footer">
    English (India) • GitHub Pages Ready
  </div>
</div>

<script>
let videoFile;

document.getElementById("videoInput").addEventListener("change", e => {
  videoFile = e.target.files[0];
  if(!videoFile) return;

  if(videoFile.size > 300 * 1024 * 1024){
    alert("Video too large (Max 300MB)");
    videoFile = null;
    return;
  }

  document.getElementById("status").innerText =
    "Video selected: " + videoFile.name;
});

function generateCaptions(){
  if(!videoFile){
    alert("Please select a video first");
    return;
  }

  const btn = document.getElementById("genBtn");
  btn.disabled = true;
  document.getElementById("status").innerText = "Processing...";
  document.getElementById("captions").innerText = "";

  // Demo caption (API placeholder)
  setTimeout(() => {
    document.getElementById("captions").innerText =
`Hello everyone,
this is an auto caption demo.
Language selected: English (India).
You can connect real Speech-to-Text API here.`;

    document.getElementById("status").innerText = "Captions generated ✔";
    btn.disabled = false;
  }, 2000);
}
</script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Auto Caption Video</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body{
  margin:0;
  font-family:Arial, sans-serif;
  background:#0b0b0b;
  color:#fff;
}
.container{
  max-width:600px;
  margin:auto;
  padding:20px;
}
h1{
  text-align:center;
  color:#00ffcc;
}
.card{
  background:#151515;
  padding:20px;
  border-radius:8px;
}
input[type=file]{
  width:100%;
  padding:10px;
  background:#000;
  color:#fff;
  border:1px solid #333;
}
button{
  width:100%;
  margin-top:12px;
  padding:12px;
  background:#00ffcc;
  border:none;
  font-size:16px;
  cursor:pointer;
}
button:disabled{
  background:#555;
}
#status{
  margin-top:10px;
  font-size:14px;
}
#captions{
  margin-top:15px;
  background:#000;
  padding:10px;
  height:200px;
  overflow:auto;
  border:1px solid #333;
  white-space:pre-line;
}
.footer{
  text-align:center;
  margin-top:15px;
  font-size:12px;
  color:#777;
}
</style>
</head>

<body>
<div class="container">
  <h1>Auto Caption Video</h1>

  <div class="card">
    <input type="file" id="videoInput" accept="video/*">
    <button id="genBtn" onclick="generateCaptions()">Generate Captions</button>
    <div id="status"></div>
    <div id="captions"></div>
  </div>

  <div class="footer">
    English (India) • GitHub Pages Ready
  </div>
</div>

<script>
let videoFile;

document.getElementById("videoInput").addEventListener("change", e => {
  videoFile = e.target.files[0];
  if(!videoFile) return;

  if(videoFile.size > 300 * 1024 * 1024){
    alert("Video too large (Max 300MB)");
    videoFile = null;
    return;
  }

  document.getElementById("status").innerText =
    "Video selected: " + videoFile.name;
});

function generateCaptions(){
  if(!videoFile){
    alert("Please select a video first");
    return;
  }

  const btn = document.getElementById("genBtn");
  btn.disabled = true;
  document.getElementById("status").innerText = "Processing...";
  document.getElementById("captions").innerText = "";

  // Demo caption (API placeholder)
  setTimeout(() => {
    document.getElementById("captions").innerText =
`Hello everyone,
this is an auto caption demo.
Language selected: English (India).
You can connect real Speech-to-Text API here.`;

    document.getElementById("status").innerText = "Captions generated ✔";
    btn.disabled = false;
  }, 2000);
}
</script>
</body>
</html>

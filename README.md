<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Nice ra ang bracelet? </title>
  <style>
    body {
      margin: 0;
      font-family: 'Comic Sans MS', cursive, sans-serif;
      background: linear-gradient(120deg, #ff9a9e, #fad0c4);
      color: #333;
      text-align: center;
      padding: 40px;
    }
    h1 {
      margin-top: 60px;
      font-size: 2.5em;
    }
    .btn {
      display: inline-block;
      margin: 20px;
      padding: 12px 25px;
      background: #ff6f91;
      color: white;
      border-radius: 10px;
      font-size: 1.2em;
      cursor: pointer;
      border: none;
      transition: 0.3s;
    }
    .btn:hover {
      background: #ff3e71;
    }
    #message {
      margin-top: 40px;
      font-size: 1.5em;
      color: #ff3e71;
      display: none;
    }
    #playlist, #photos {
      margin-top: 30px;
      display: none;
    }
    #photos img {
      width: 200px;
      height: auto;
      margin: 10px;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
      transition: transform 0.3s;
    }
    #photos img:hover {
      transform: scale(1.05);
    }
    /* Trick for "No" button */
    #noBtn {
      position: absolute;
    }
  </style>
</head>
<body>
  <h1>Nice ra ang bracelet? 🤔</h1>

  <button class="btn" onclick="showYes()">Yes 👍🏻</button>
  <button class="btn" id="noBtn" onmouseover="moveButton()">No 👎🏻</button>

  <p id="message">YOWNN, i hope you appreciate it buta👓 🫶🏻</p>

  <div id="playlist">
    <iframe style="border-radius:12px" 
      src="https://open.spotify.com/embed/playlist/36v9lqv7zBKaehXpgi3Yot?si=AF4aWfKyRxi8FajdWvBNxw&pi=-N9s2HdIQzG1C" 
      width="100%" height="380" frameBorder="0" 
      allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" 
      loading="lazy"></iframe>
  </div>

  <div id="photos">
    <h2>🫰🏻</h2>
    <img src="https://drive.google.com/file/d/1TBepOmzFF2FznkYMn4uUIwMuC-2f-k4E/view?usp=drivesdk" alt="🥰">
    <img src="https://drive.google.com/file/d/1p3twFUfUgaGOJ0VXqe1tsj0B50OqMX4Z/view?usp=drivesdk" alt="👻">
    <img src="https://drive.google.com/file/d/1TBepOmzFF2FznkYMn4uUIwMuC-2f-k4E/view?usp=drivesdk" alt="🤪">
  </div>

  <script>
    function showYes() {
      document.getElementById('message').style.display = 'block';
      document.getElementById('playlist').style.display = 'block';
      document.getElementById('photos').style.display = 'block';
    }
    function moveButton() {
      let x = Math.floor(Math.random() * (window.innerWidth - 100));
      let y = Math.floor(Math.random() * (window.innerHeight - 100));
      document.getElementById('noBtn').style.left = x + "px";
      document.getElementById('noBtn').style.top = y + "px";
    }
  </script>
</body>
</html>
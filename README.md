<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Лампа Kalaisyn Bro</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      background-color: #f0f0f0;
    }

    .lamp {
      margin-top: 50px;
      width: 150px;
      height: 150px;
      border-radius: 50%;
      background-color: #555;
      display: flex;
      justify-content: center;
      align-items: center;
      color: transparent;
      font-weight: bold;
      font-size: 18px;
      transition: background-color 0.5s, color 0.5s;
    }

    .lamp.on {
      background-color: yellow;
      color: #000;
      box-shadow: 0 0 30px yellow;
    }

    .button-container {
      margin-bottom: 40px;
    }

    button {
      padding: 12px 24px;
      font-size: 16px;
      background-color: #ccc;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    button:hover {
      background-color: #bbb;
    }
  </style>
</head>
<body>

  <div class="lamp" id="lamp">kalaisyn Bro</div>

  <div class="button-container">
    <button onclick="toggleLamp()">Нажми сюда</button>
  </div>

  <!-- Звук щелчка -->
  <audio id="switch-sound">
    <source src="https://www.soundjay.com/button/sounds/button-16.mp3" type="audio/mpeg">
    Ваш браузер не поддерживает аудио.
  </audio>

  <script>
    function toggleLamp() {
      const lamp = document.getElementById('lamp');
      const sound = document.getElementById('switch-sound');
      
      lamp.classList.toggle('on');
      sound.currentTime = 0; // сбрасываем на начало
      sound.play();
    }
  </script>

</body>
</html>

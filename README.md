<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Meu Perfil no GitHub</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Meu Perfil no GitHub</h1>
    <p>Bem-vindo ao meu perfil! Veja abaixo a animação de perfil.</p>
  </header>

  <div class="snake-container" id="snakeContainer">
    <div class="snake" id="snake"></div>
  </div>

  <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    background-color: #f0f0f0;
  }

  header {
    text-align: center;
  }

  .snake-container {
    position: relative;
    width: 200px;
    height: 200px;
    border: 1px solid #000;
    overflow: hidden;
  }

  .snake {
    position: absolute;
    background-color: #ff0000;
    width: 20px;
    height: 20px;
  }
  document.addEventListener("DOMContentLoaded", function() {
    const snake = document.getElementById("snake");
    const container = document.getElementById("snakeContainer");

    container.addEventListener("mousemove", function(e) {
      const x = e.clientX - container.offsetLeft - (snake.offsetWidth / 2);
      const y = e.clientY - container.offsetTop - (snake.offsetHeight / 2);

      snake.style.left = `${x}px`;
      snake.style.top = `${y}px`;
    });
  });

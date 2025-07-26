# -Dice-Roller-Simulator
A simple and fun web-based dice roller built using HTML, CSS, and JavaScript. Click the button to roll a virtual dice and get a random result (⚀ to ⚅). Great for learning basic DOM manipulation and event handling in JavaScript.

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Dice Roller Simulator</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: #f0f0f0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .container {
      text-align: center;
      background: white;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    }

    .dice {
      font-size: 100px;
      margin: 20px 0;
    }

    button {
      padding: 10px 25px;
      font-size: 18px;
      border: none;
      background-color: #4CAF50;
      color: white;
      border-radius: 8px;
      cursor: pointer;
      transition: background 0.3s;
    }

    button:hover {
      background-color: #388e3c;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>🎲 Dice Roller Simulator</h1>
    <div id="dice" class="dice">⚀</div>
    <button onclick="rollDice()">Roll Dice</button>
  </div>

  <script>
    function rollDice() {
      const diceFaces = ["⚀", "⚁", "⚂", "⚃", "⚄", "⚅"];
      const randomIndex = Math.floor(Math.random() * 6);
      document.getElementById("dice").innerHTML = diceFaces[randomIndex];
    }
  </script>
</body>
</html>

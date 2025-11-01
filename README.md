# I-love-you-game
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>I Love You ❤️</title>
  <style>
    body {
      background: linear-gradient(135deg, #ffb6c1, #ff69b4);
      text-align: center;
      font-family: 'Poppins', sans-serif;
      height: 100vh;
      margin: 0;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
    h1 {
      color: white;
      font-size: 2.5em;
      margin-bottom: 10px;
      text-shadow: 2px 2px 5px rgba(0,0,0,0.3);
    }
    p {
      font-size: 1.2em;
      color: white;
      margin-bottom: 30px;
    }
    button {
      font-size: 1.2em;
      padding: 12px 25px;
      margin: 15px;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      transition: all 0.3s ease;
    }
    #yesBtn {
      background-color: #4CAF50;
      color: white;
    }
    #noBtn {
      background-color: #ff4444;
      color: white;
      position: absolute;
    }
  </style>
</head>
<body>
  <h1>I Love You 💖</h1>
  <p>Do you love me too?</p>
  <button id="yesBtn" onclick="sayYes()">Yes</button>
  <button id="noBtn" onmouseover="moveNo()">No</button>

  <script>
    const noBtn = document.getElementById('noBtn');

    function moveNo() {
      const x = Math.random() * (window.innerWidth - 100);
      const y = Math.random() * (window.innerHeight - 100);
      noBtn.style.left = `${x}px`;
      noBtn.style.top = `${y}px`;
    }

    function sayYes() {
      document.body.innerHTML = `
        <div style="text-align:center; color:white; font-size:2em; padding:20px;">
          ❤️ Yay! I love you too! ❤️<br><br>
          <small>Thanks for saying YES 💕</small>
        </div>`;
    }
  </script>
</body>
</html>

<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>چرخ شانسی</title>
  <style>
    body {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      background: #1a202c;
      color: white;
      font-family: sans-serif;
    }
    button {
      background: #4299e1;
      color: white;
      padding: 12px 24px;
      font-size: 18px;
      border: none;
      border-radius: 12px;
      cursor: pointer;
    }
    button:disabled {
      background: gray;
      cursor: not-allowed;
    }
    p {
      margin-top: 20px;
      font-size: 20px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>🎡 چرخ شانسی</h1>
  <button id="spinBtn">شروع کن</button>
  <p id="result"></p>

  <script>
    const prizes = ["1 دلار", "2 دلار", "5 دلار", "10 دلار", "NFT رایگان", "بدون جایزه"];
    const btn = document.getElementById("spinBtn");
    const result = document.getElementById("result");

    btn.addEventListener("click", () => {
      btn.disabled = true;
      result.textContent = "در حال چرخش...";
      setTimeout(() => {
        const random = Math.floor(Math.random() * prizes.length);
        result.textContent = "نتیجه: " + prizes[random];
        btn.disabled = false;
      }, 2000);
    });
  </script>
</body>
</html>

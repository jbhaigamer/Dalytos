<!doctype html>
<html lang="hi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>₹1 सिक्का Toss</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background: #f4f6f9;
      margin: 0;
      padding: 0;
    }
    h1 {
      background: #0078ff;
      color: #fff;
      padding: 15px;
      margin: 0;
    }
    .coin {
      width: 150px;
      height: 150px;
      margin: 40px auto;
      perspective: 1000px;
    }
    .coin-inner {
      width: 100%;
      height: 100%;
      position: relative;
      transform-style: preserve-3d;
      transition: transform 2s;
    }
    .side {
      position: absolute;
      width: 100%;
      height: 100%;
      border-radius: 50%;
      backface-visibility: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 22px;
      font-weight: bold;
      color: white;
    }
    .head {
      background: gold url('https://i.ibb.co/Chjv1D5/indian-rupee-head.png') center/cover no-repeat;
    }
    .tail {
      background: goldenrod url('https://i.ibb.co/jkbLf4c/indian-rupee-tail.png') center/cover no-repeat;
      transform: rotateY(180deg);
    }
    button {
      padding: 12px 24px;
      font-size: 18px;
      margin-top: 20px;
      background: #0078ff;
      color: #fff;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }
    .result {
      margin-top: 20px;
      font-size: 20px;
      font-weight: bold;
      color: #333;
    }
  </style>
</head>
<body>
  <h1>₹1 सिक्का Toss</h1>
  <div class="coin">
    <div class="coin-inner" id="coin">
      <div class="side head">Head</div>
      <div class="side tail">Tail</div>
    </div>
  </div>
  <button onclick="tossCoin()">Toss करें</button>
  <div class="result" id="result">👉 Toss करने के लिए बटन दबाएँ</div>

  <script>
    function tossCoin() {
      const coin = document.getElementById('coin');
      const result = document.getElementById('result');
      const toss = Math.random() < 0.5 ? "Head" : "Tail";

      if (toss === "Head") {
        coin.style.transform = "rotateY(0deg) rotate(3600deg)";
        result.textContent = "🎉 Result: Head आया";
      } else {
        coin.style.transform = "rotateY(180deg) rotate(3600deg)";
        result.textContent = "🎉 Result: Tail आया";
      }
    }
  </script>
</body>
</html># Dalytos
Easy to use single tap to pause choice

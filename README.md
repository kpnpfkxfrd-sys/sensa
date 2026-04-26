# sensa
Digital storefront for PUBG sensitivity configs integrated with Telegram bot payments and WebApp UI.
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>PUBG Shop</title>

  <script src="https://telegram.org/js/telegram-web-app.js"></script>

  <style>
    body {
      background: #0f172a;
      color: white;
      font-family: Arial;
      text-align: center;
      padding: 20px;
    }

    .card {
      background: #1e293b;
      padding: 20px;
      margin: 15px;
      border-radius: 12px;
    }

    button {
      width: 100%;
      margin-top: 10px;
      padding: 12px;
      border-radius: 10px;
      border: none;
      font-size: 16px;
      color: white;
      cursor: pointer;
    }

    .buy {
      background: #22c55e;
    }

    .discount {
      background: #3b82f6;
    }

    .back {
      background: #334155;
    }
  </style>
</head>

<body>

<h2>🔥 PUBG Sens Shop</h2>

<div class="card">
  <p>Выбери вариант покупки</p>

  <button class="buy" onclick="buy('full')">
    Купить — 1000₽
  </button>

  <button class="discount" onclick="buy('discount')">
    С другом -10% → 900₽
  </button>

  <button class="back" onclick="Telegram.WebApp.close()">
    ⏪ Назад
  </button>
</div>

<script>
  Telegram.WebApp.ready();

  function buy(type) {
    Telegram.WebApp.sendData(type);
  }
</script>

</body>
</html>

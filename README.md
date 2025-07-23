<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Davlatbek Xayrullayev</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      background-color: #000;
      color: #fff;
      font-family: 'Courier New', Courier, monospace;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      padding: 20px;
    }

    .container {
      max-width: 800px;
      width: 100%;
      text-align: center;
      border: 2px solid white;
      border-radius: 20px;
      padding: 30px;
      background-color: rgba(0,0,0,0.8);
      box-shadow: 0 0 25px rgba(255, 255, 255, 0.2);
      animation: fadeIn 2s ease-in-out;
    }

    @keyframes fadeIn {
      from {opacity: 0; transform: translateY(20px);}
      to {opacity: 1; transform: translateY(0);}
    }

    h1 {
      font-size: 2.8rem;
      color: #00ffcc;
      margin-bottom: 15px;
    }

    .typing {
      font-size: 1.3rem;
      color: #aaa;
      margin-bottom: 20px;
      height: 30px;
    }

    .about {
      margin-top: 25px;
      text-align: left;
    }

    .about h2 {
      color: #00ffcc;
      margin-bottom: 10px;
    }

    .about p {
      font-size: 1.1rem;
      line-height: 1.6;
    }

    .buttons {
      margin-top: 30px;
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 15px;
    }

    button {
      background-color: #00ffcc;
      color: #000;
      border: none;
      padding: 10px 20px;
      border-radius: 10px;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s ease;
    }

    button:hover {
      background-color: #fff;
      transform: scale(1.05);
      box-shadow: 0 0 10px #00ffcc;
    }

    .quote {
      margin-top: 25px;
      font-style: italic;
      color: #888;
    }

    @media (max-width: 600px) {
      h1 {
        font-size: 2rem;
      }
      .about p {
        font-size: 1rem;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Salom, men Davlatbek Xayrullayev</h1>
    <p class="typing" id="typing"></p>

    <div class="about">
      <h2>🧠 Men haqimda</h2>
      <p>Men zamonaviy frontend dasturchiman. HTML, CSS va JavaScript texnologiyalari orqali kreativ, mobilga mos saytlar yarataman. Hozircha mustaqil ishlayman, lekin katta jamoada ishlash orzum bor.</p>
    </div>

    <div class="quote" id="quote"></div>

    <div class="buttons">
      <button onclick="changeTheme()">🌙 Mavzuni o‘zgartir</button>
      <button onclick="alertInfo()">ℹ️ Ma’lumot</button>
      <button onclick="location.reload()">🔁 Qayta yuklash</button>
    </div>
  </div>

  <script>
    // Typing effekt
    const typingText = "HTML | CSS | JavaScript | Portfolio | Mustaqil dasturchi";
    let index = 0;
    const typingElement = document.getElementById("typing");

    function type() {
      typingElement.textContent = typingText.slice(0, index++);
      if (index > typingText.length) {
        index = 0;
        setTimeout(type, 1200);
      } else {
        setTimeout(type, 100);
      }
    }
    type();

    // Mavzu almashtirish
    function changeTheme() {
      const body = document.body;
      const container = document.querySelector('.container');

      if (body.style.backgroundColor === "white") {
        body.style.backgroundColor = "#000";
        body.style.color = "#fff";
        container.style.backgroundColor = "rgba(0,0,0,0.8)";
        container.style.borderColor = "#fff";
      } else {
        body.style.backgroundColor = "#fff";
        body.style.color = "#000";
        container.style.backgroundColor = "#f9f9f9";
        container.style.borderColor = "#000";
      }
    }

    // Ma’lumot tugmasi
    function alertInfo() {
      alert("Davlatbek Xayrullayev\nFrontend Developer\nSayt: HTML + CSS + JavaScript");
    }

    // Random quote
    const quotes = [
      "Har bir kod — bu imkoniyat!",
      "Bugun yozgan koding ertangi kelajaging!",
      "Kod yoz, xatolar o‘rgatadi!",
      "O‘z yo‘lingni o‘zing yoz!",
      "Dasturlash – bu yangi dunyo yaratishdir!"
    ];
    document.getElementById("quote").textContent = `"${quotes[Math.floor(Math.random() * quotes.length)]}"`;
  </script>
</body>
</html>

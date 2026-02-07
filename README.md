<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Happy Rose Day Supriya 🌹</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ff5f7e, #ff9a9e);
      color: white;
      text-align: center;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }
    .card {
      background: rgba(255, 255, 255, 0.12);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      padding: 30px 25px 40px;
      max-width: 420px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.2);
      animation: fadeIn 1.5s ease;
      position: relative;
      z-index: 2;
    }
    h1 {
      font-size: 2.2rem;
      margin-bottom: 10px;
    }
    .rose {
      font-size: 3.5rem;
      margin: 15px 0;
      animation: float 2.5s infinite ease-in-out;
    }
    p {
      font-size: 1.05rem;
      line-height: 1.6;
      margin: 15px 0;
    }
    .heart-btn {
      margin-top: 20px;
      padding: 14px 30px;
      font-size: 1.1rem;
      border-radius: 40px;
      border: none;
      background: white;
      color: #ff4b6e;
      font-weight: bold;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 10px;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .heart-btn:hover {
      transform: scale(1.08);
      box-shadow: 0 10px 25px rgba(0,0,0,0.25);
    }
    .hidden {
      display: none;
    }
    .gojo {
      position: absolute;
      bottom: -220px;
      left: 50%;
      transform: translateX(-50%);
      width: 180px;
      animation: rise 1.5s ease forwards;
      z-index: 1;
    }
    .petal {
      position: absolute;
      top: -20px;
      font-size: 1.2rem;
      animation: fall linear forwards;
      opacity: 0.9;
    }
    .footer {
      margin-top: 20px;
      font-size: 0.9rem;
      opacity: 0.85;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
    @keyframes rise {
      to { bottom: 20px; }
    }
    @keyframes fall {
      to { transform: translateY(110vh) rotate(360deg); }
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>Happy Rose Day, Supriya 🌹</h1>
    <div class="rose">🌹</div>
    <p>
      This rose is for you —
      for your smile, your warmth,
      and the way you make my world softer.
    </p><button class="heart-btn" onclick="revealLove()">
  ❤️ Click Here
</button>

<div class="footer">
  — Yours, always
</div>

  </div>  <!-- Gojo Chibi (image) -->  <img id="gojo" class="gojo hidden" src="https://i.imgur.com/9Z6QZ9F.png" alt="Gojo chibi carrying rose" />  <!-- Romantic Music --><audio id="music" src="https://cdn.pixabay.com/audio/2022/03/15/audio_4c5c3b5c3f.mp3"></audio>

  <script>
    function revealLove() {
      const gojo = document.getElementById('gojo');
      const music = document.getElementById('music');

      gojo.classList.remove('hidden');
      music.play();

      for (let i = 0; i < 20; i++) {
        const petal = document.createElement('div');
        petal.className = 'petal';
        petal.innerText = '🌹';
        petal.style.left = Math.random() * 100 + 'vw';
        petal.style.animationDuration = (3 + Math.random() * 3) + 's';
        document.body.appendChild(petal);

        setTimeout(() => petal.remove(), 6000);
      }
    }
  </script></body>
</html>

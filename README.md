<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mi Vidita 🤍</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background-color: #1a001f;
      overflow: hidden;
      font-family: "Poppins", sans-serif;
      color: white;
      text-align: center;
    }

    /* corazones flotando */
    .heart {
      position: fixed;
      color: #d8b3ff;
      font-size: 20px;
      animation: float 6s linear infinite;
    }

    @keyframes float {
      0% {transform: translateY(0) scale(1);}
      100% {transform: translateY(-100vh) scale(0.8);}
    }

    h1 {
      color: #d8b3ff;
      margin-top: 120px;
      font-size: 48px;
      text-shadow: 0 0 10px #b266ff;
    }

    img {
      width: 220px;
      margin-top: 15px;
    }

    .icons {
      margin-top: 30px;
      font-size: 35px;
      cursor: pointer;
      color: white;
    }

    .btn-love {
      background-color: #b266ff;
      color: white;
      border: none;
      padding: 15px 30px;
      border-radius: 40px;
      font-size: 20px;
      margin-top: 40px;
      cursor: pointer;
      transition: 0.3s;
    }

    .btn-love:hover {
      background-color: #d8b3ff;
      color: #1a001f;
    }

    /* ventana de carta */
    .overlay {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      justify-content: center;
      align-items: center;
    }

    .card {
      background-color: white;
      color: #4a0066;
      padding: 40px;
      border-radius: 20px;
      max-width: 500px;
      text-align: left;
      font-size: 16px;
      line-height: 1.5;
      box-shadow: 0 0 30px rgba(255, 255, 255, 0.3);
      animation: fadeIn 1s ease;
    }

    @keyframes fadeIn {
      from {opacity: 0; transform: scale(0.8);}
      to {opacity: 1; transform: scale(1);}
    }

    .close-btn {
      display: block;
      margin: 20px auto 0;
      background-color: #b266ff;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 30px;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <h1>Mi vidita</h1>
  <img src="https://i.ibb.co/ZVhHb5d/lirios.png" alt="Lirios">

  <div class="icons">
    🎵
  </div>

  <button class="btn-love" id="loveBtn">Te amo  🤍</button>

  <div class="overlay" id="overlay">
    <div class="card">
      <p>
        Mi amor, quiero desearte toda la suerte del mundo en esta nueva etapa de tu vida. Sé que estás por comenzar algo muy importante, y quiero que sepas que me siento tan feliz por ti, por todo lo que estás logrando y por todo lo que aún te falta por vivir. La universidad es un nuevo camino lleno de oportunidades, aprendizajes y momentos que te van a marcar, y estoy segura de que vas a brillar como siempre lo haces.<br><br>

        Eres una persona increíblemente dedicada, inteligente, y con un corazón enorme. Todo lo que haces lo haces con pasión, y por eso sé que cada esfuerzo valdrá la pena. Habrá días buenos y días difíciles, pero quiero que nunca olvides lo capaz que eres y todo lo que ya has superado. Cada paso, cada clase, cada logro será parte de tu crecimiento, y yo voy a estar ahí para acompañarte, apoyarte y recordarte siempre lo mucho que vales.<br><br>

        Me siento tan orgullosa de ti, de todo lo que has alcanzado y de la manera en que sigues adelante sin rendirte. Ver cómo vas cumpliendo tus metas me llena de alegría, porque sé que detrás de todo hay esfuerzo, ganas y un corazón enorme. Estoy segura de que esta nueva etapa te va a traer cosas maravillosas, personas nuevas, experiencias únicas y muchos motivos más para sonreír.<br><br>

        Quiero que sepas que creo en ti con todo mi corazón. Pase lo que pase, siempre voy a estar aquí, alentándote y admirando la persona tan increíble que eres. Te amo con todo mi ser, y te deseo toda la suerte, la fuerza y la felicidad del mundo en esta nueva etapa.🤍<br><br>

        Ve con todo, mi vida, que el mundo necesita ver todo lo bonito que llevas dentro.
      </p>
      <button class="close-btn" id="closeBtn">Cerrar</button>
    </div>
  </div>

  <audio id="song" src="https://www.w3schools.com/html/horse.mp3"></audio>

  <script>
    // corazones flotando
    for (let i = 0; i < 20; i++) {
      let heart = document.createElement('div');
      heart.className = 'heart';
      heart.innerHTML = '🤍';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = 4 + Math.random() * 3 + 's';
      document.body.appendChild(heart);
    }

    // música
    const song = document.getElementById('song');
    const musicIcon = document.querySelector('.icons');
    musicIcon.addEventListener('click', () => {
      song.play();
    });

    // carta
    const overlay = document.getElementById('overlay');
    const loveBtn = document.getElementById('loveBtn');
    const closeBtn = document.getElementById('closeBtn');

    loveBtn.addEventListener('click', () => {
      overlay.style.display = 'flex';
    });

    closeBtn.addEventListener('click', () => {
      overlay.style.display = 'none';
    });
  </script>
</body>
</html>

<html lang="es">
<head>
  
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

    /* Reset */
    * {
      margin: 0; padding: 0; box-sizing: border-box;
    }
    body {
      background: linear-gradient(135deg, #0d001f, #2a004f);
      color: #d6d0ff;
      font-family: 'Poppins', sans-serif;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 50px 20px;
      user-select: none;
    }

    header {
      width: 100%;
      max-width: 1200px;
      display: flex;
      justify-content: flex-start;
      align-items: center;
      margin-bottom: 60px;
    }
    .logo {
      height: 80px;
      filter: drop-shadow(0 0 12px #6b4fff);
      transition: transform 0.4s ease;
      cursor: pointer;
    }
    .logo:hover {
      transform: scale(1.15) rotate(-7deg);
      filter: drop-shadow(0 0 20px #937fff);
    }

    h1 {
      font-size: 3.6rem;
      font-weight: 700;
      text-align: center;
      text-shadow: 0 0 15px #7f5fff;
      max-width: 900px;
      margin-bottom: 18px;
      letter-spacing: 2px;
      user-select: text;
    }

    p.subtitle {
      max-width: 720px;
      font-size: 1.3rem;
      color: #b9b0ffcc;
      text-align: center;
      margin-bottom: 70px;
      line-height: 1.6;
      text-shadow: 0 0 8px #6244ffbb;
      user-select: text;
    }

    .platforms {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(240px,1fr));
      gap: 38px;
      width: 100%;
      max-width: 1100px;
      padding: 0 10px;
    }

    .card {
      background: #1a1140;
      border-radius: 20px;
      padding: 30px 25px;
      box-shadow:
        0 0 30px #5f47ff88,
        inset 0 0 12px #927aff88;
      color: #cecaff;
      cursor: pointer;
      transition: transform 0.4s ease, box-shadow 0.4s ease;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      user-select: none;
      position: relative;
      perspective: 900px;
      border: 2px solid transparent;
    }

    .card:hover {
      transform: translateY(-18px) rotateX(9deg) rotateY(14deg);
      box-shadow:
        0 0 60px #8a73ffcc,
        inset 0 0 20px #b3a5ffcc;
      border-color: #a992ff;
      z-index: 20;
    }

    .card img {
      max-width: 140px;
      margin-bottom: 22px;
      filter: drop-shadow(0 0 12px #6c5fffcc);
      border-radius: 0;
      height: auto;
      object-fit: contain;
      transition: filter 0.4s ease;
    }

    .card:hover img {
      filter: drop-shadow(0 0 26px #b6a9ff);
    }

    /* Aquí cambió la estructura para separar nombre y precio */
    .card h3 {
      font-size: 1.7rem;
      color: #b8aaff;
      text-shadow: 0 0 12px #9984ff;
      letter-spacing: 1.2px;
      user-select: text;
      margin-bottom: 8px;
    }

    .price {
      font-size: 1.3rem;
      font-weight: 700;
      color: #ffcc66;
      text-shadow: 0 0 8px #ffcc00;
      user-select: text;
      margin-bottom: 15px;
    }

    .card p {
      font-size: 1.05rem;
      line-height: 1.5;
      color: #b3acffcc;
      min-height: 80px;
      user-select: text;
    }

    .btn-cta {
      margin-top: 75px;
      background: linear-gradient(90deg, #3d2fd5, #8a78ff);
      border: none;
      padding: 20px 65px;
      border-radius: 50px;
      font-size: 1.45rem;
      font-weight: 700;
      color: #e0ddff;
      cursor: pointer;
      box-shadow:
        0 0 40px #846fff,
        inset 0 0 20px #c3baff;
      transition: all 0.5s ease;
      text-transform: uppercase;
      letter-spacing: 2px;
      user-select: none;
      position: relative;
      overflow: hidden;
      filter: drop-shadow(0 0 25px #8e7fff);
    }

    .btn-cta::before {
      content: '';
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: linear-gradient(45deg, rgba(255,255,255,0.7), rgba(255,255,255,0));
      transform: rotate(45deg);
      transition: all 0.6s ease;
      pointer-events: none;
      filter: blur(28px);
      animation: shine 3.5s infinite linear;
      z-index: 1;
    }
    @keyframes shine {
      0% {
        transform: translateX(-100%) rotate(45deg);
      }
      100% {
        transform: translateX(100%) rotate(45deg);
      }
    }
    .btn-cta:hover {
      background: linear-gradient(90deg, #5f55ff, #b0aaff);
      box-shadow:
        0 0 60px #a89fff,
        inset 0 0 35px #d7ccff;
      filter: drop-shadow(0 0 35px #b9aaff);
    }

    footer {
      margin-top: 90px;
      font-size: 0.9rem;
      color: #9a8ffcaa;
      text-align: center;
      user-select: none;
    }

    /* Responsive */
    @media (max-width: 720px) {
      h1 {
        font-size: 2.8rem;
      }
      p.subtitle {
        font-size: 1.1rem;
      }
      .card {
        padding: 25px 18px;
      }
      .card img {
        max-width: 110px;
      }
      .card h3 {
        margin-bottom: 5px;
      }
      .price {
        margin-bottom: 12px;
      }
    }
  </style>
</head>
<body>

<header>
  <img src="logo.png" alt="Logo Vendo" class="logo" />
</header>

<h1>Tu Portal Premium de Streaming</h1>
<p class="subtitle">
  Netflix, HBO Max, Prime Video, Disney+, Star+, Paramount+, Apple TV+, Hulu, Peacock y más en un solo lugar con estilo oscuro y la mejor calidad visual.
</p>

<div class="platforms" role="list" aria-label="Plataformas de streaming disponibles">
  <article class="card" role="listitem" tabindex="0" aria-label="Netflix">
    <img src="https://upload.wikimedia.org/wikipedia/commons/0/08/Netflix_2015_logo.svg" alt="Logo Netflix" />
    <h3>Netflix</h3>
    <div class="price">L80</div>
    <p>Accede a series y películas exclusivas en una plataforma líder mundial.</p>
  </article>

  <article class="card" role="listitem" tabindex="0" aria-label="HBO Max">
    <img src="https://upload.wikimedia.org/wikipedia/commons/1/17/HBO_Max_Logo.svg" alt="Logo HBO Max" />
    <h3>HBO Max</h3>
    <div class="price">L80</div>
    <p>Disfruta contenido premium de Warner Bros, DC, y mucho más.</p>
  </article>

  <article class="card" role="listitem" tabindex="0" aria-label="Prime Video">
    <img src="https://upload.wikimedia.org/wikipedia/commons/f/f1/Prime_Video.png" alt="Logo Prime Video" />
    <h3>Prime Video</h3>
    <div class="price">L80</div>
    <p>Explora un catálogo extenso con estrenos y clásicos del cine y TV.</p>
  </article>

  <article class="card" role="listitem" tabindex="0" aria-label="Disney+">
    <img src="https://upload.wikimedia.org/wikipedia/commons/3/3e/Disney%2B_logo.svg" alt="Logo Disney+" />
    <h3>Disney+</h3>
    <div class="price">L130</div>
    <p>Los mejores universos de Disney, Marvel, Star Wars y Pixar a tu alcance.</p>
  </article>

  <article class="card" role="listitem" tabindex="0" aria-label="Star+">
    <img src="star.png" alt="Logo Star+" />
    <h3>Star+</h3>
    <div class="price">L130</div>
    <p>Series y películas exclusivas para toda la familia y adultos.</p>
  </article>

  <article class="card" role="listitem" tabindex="0" aria-label="Paramount+">
    <img src="paramount.png" alt="Logo Paramount+" />
    <h3>Paramount+</h3>
    <div class="price">L80</div>
    <p>Grandes franquicias, noticias y deportes en vivo.</p>
  </article>

  <article class="card" role="listitem" tabindex="0" aria-label="Apple TV+">
    <img src="appl.png" alt="Logo Apple TV+" />
    <h3>Apple TV+</h3>
    <div class="price">L130</div>
    <p>Contenido original con calidad cinematográfica y exclusivas.</p>
  </article>

  <article class="card" role="listitem" tabindex="0" aria-label="Hulu">
    <img src="hulu.png" alt="Logo Hulu" />
    <h3>Hulu</h3>
    <div class="price">L80</div>
    <p>Series, películas y programas con actualización frecuente.</p>
  </article>


</div>


<button class="btn-cta" aria-label="Suscríbete ahora" id="btnWhatsapp">Comprar suscripción</button>

<script>
  const btnWhatsapp = document.getElementById('btnWhatsapp');
  btnWhatsapp.addEventListener('click', () => {
    const phone = '50488655980'; // tu número sin espacios ni signos
    const url = `https://wa.me/${phone}`;
    window.open(url, '_blank');
  });
</script>

<footer>
  IDSMORGAN &copy; 2025
</footer>

</body>
</html>

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Renacer el Alma — Sanación Holística</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Lora:wght@400;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --rosa-pastel: #f9d6e0;
      --crema: #fdfbf7;
      --rosa-intenso: #e8a5c4;
      --blanco-roto: #fffaf3;
      --dorado-suave: #f5d7a1;
      --texto: #7a5b7a;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Lora', serif;
      background-color: var(--crema);
      color: var(--texto);
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* Header */
    header {
      background: rgba(255, 255, 255, 0.9);
      backdrop-filter: blur(5px);
      padding: 1rem 2rem;
      position: fixed;
      width: 100%;
      z-index: 100;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid var(--rosa-pastel);
    }

    .logo {
      font-family: 'Playfair Display', serif;
      font-size: 1.8rem;
      font-weight: bold;
      color: var(--rosa-intenso);
      letter-spacing: 1px;
    }

    nav ul {
      display: flex;
      list-style: none;
    }

    nav li a {
      color: var(--texto);
      text-decoration: none;
      padding: 0.5rem 1rem;
      margin-left: 1rem;
      border-radius: 20px;
      transition: all 0.3s ease;
    }

    nav li a:hover {
      background: var(--rosa-pastel);
      color: var(--rosa-intenso);
    }

    /* Hero Section */
    .hero {
      height: 100vh;
      background: url('https://i.imgur.com/8KQVqkZ.png') center center;
      background-size: cover;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: var(--blanco-roto);
      position: relative;
    }

    .hero::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.3));
    }

    .hero h1 {
      font-family: 'Playfair Display', serif;
      font-size: 2.2rem;
      margin-bottom: 1rem;
      max-width: 800px;
      text-shadow: 2px 2px 6px rgba(0,0,0,0.6);
      line-height: 1.4;
    }

    .hero p {
      font-size: 1.1rem;
      max-width: 700px;
      margin: 0 auto 1.5rem;
      text-shadow: 1px 1px 4px rgba(0,0,0,0.6);
    }

    .btn {
      background: var(--rosa-intenso);
      color: white;
      padding: 0.8rem 1.8rem;
      border-radius: 30px;
      text-decoration: none;
      font-weight: bold;
      font-family: 'Playfair Display', serif;
      transition: all 0.3s ease;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }

    .btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 14px rgba(0,0,0,0.15);
    }

    /* Secciones */
    section {
      padding: 5rem 2rem;
      text-align: center;
    }

    section h2 {
      font-family: 'Playfair Display', serif;
      font-size: 2.2rem;
      margin-bottom: 2rem;
      color: var(--rosa-intenso);
    }

    /* Servicios y Productos */
    .services, .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 2rem;
      margin-top: 2rem;
    }

    .card {
      background: var(--blanco-roto);
      padding: 1.8rem;
      border-radius: 18px;
      box-shadow: 0 6px 15px rgba(232, 165, 196, 0.2);
      transition: all 0.3s ease;
      border: 1px solid var(--rosa-pastel);
    }

    .card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 20px rgba(232, 165, 196, 0.3);
    }

    .card h3 {
      color: var(--rosa-intenso);
      font-family: 'Playfair Display', serif;
      margin-bottom: 0.8rem;
    }

    .card p {
      color: #888;
      font-size: 0.95rem;
    }

    .testimonials {
      background: var(--crema);
    }

    .testimonial {
      font-style: italic;
      font-size: 1.1rem;
      max-width: 700px;
      margin: 0 auto 1.5rem;
      font-family: 'Lora', serif;
    }

    /* Footer */
    footer {
      background: var(--rosa-intenso);
      color: var(--blanco-roto);
      text-align: center;
      padding: 3rem;
      font-size: 0.95rem;
    }

    footer p {
      margin: 0.5rem 0;
    }

    /* Animación de pétalos */
    .petal {
      position: fixed;
      width: 20px;
      height: 20px;
      background: url("image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Cpath d='M50,15 C65,15 80,30 80,50 C80,65 65,80 50,80 C35,80 20,65 20,50 C20,30 35,15 50,15 Z' fill='%23f9d6e0'%3E%3C/path%3E%3C/svg%3E") no-repeat center;
      background-size: contain;
      pointer-events: none;
      z-index: 0;
      animation: fall linear forwards;
    }

    @keyframes fall {
      to {
        transform: translateY(100vh) rotate(360deg);
        opacity: 0;
      }
    }

    /* Responsive */
    @media (max-width: 768px) {
      .hero h1 { font-size: 1.8rem; }
      .hero p { font-size: 1rem; }
      nav ul { display: none; }
      section { padding: 3rem 1rem; }
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <div class="logo">Renacer el Alma</div>
    <nav>
      <ul>
        <li><a href="#inicio">Inicio</a></li>
        <li><a href="#servicios">Servicios</a></li>
        <li><a href="#productos">Productos</a></li>
        <li><a href="#testimonios">Testimonios</a></li>
        <li><a href="#contacto">Contacto</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero Section -->
  <section id="inicio" class="hero">
    <h1>Sanemos desde la raíz cualquier situación de tu vida, encontrando juntos dónde se fragmentó tu alma.</h1>
    <p>
      Cuerpo físico. Energético: chacras, meridianos, reflexología podal, auricular y de las manos, flujo espinal.<br>
      Alma: transgeneracional, karma, programas de otras vidas.<br>
      Emocional: relaciones tóxicas, niño interior, creencias limitantes, traumas, amor propio.<br>
      Y energías exteriores.<br><br>
      Limpiezas profundas para personas y espacios.<br>
      Renace contigo.
    </p>
    <a href="#servicios" class="btn">Explora mis servicios y productos</a>
  </section>

  <!-- Servicios -->
  <section id="servicios">
    <h2>Servicios de Sanación Profunda</h2>
    <div class="services">
      <div class="card">
        <h3>Sanación Física y Energética</h3>
        <p>Reequilibrio de chacras, meridianos, flujo espinal, reflexología podal, auricular y de las manos.</p>
      </div>
      <div class="card">
        <h3>Sanación del Alma</h3>
        <p>Karma, transgeneracional, memorias de otras vidas, liberación de programas ancestrales.</p>
      </div>
      <div class="card">
        <h3>Liberación Emocional</h3>
        <p>Sanación del niño interior, relaciones tóxicas, creencias limitantes, traumas, amor propio.</p>
      </div>
      <div class="card">
        <h3>Limpieza de Energías Exteriores</h3>
        <p>Protección, liberación de energías ajenas, limpieza de hogares y espacios.</p>
      </div>
    </div>
  </section>

  <!-- Productos -->
  <section id="productos" style="background: var(--rosa-pastel);">
    <h2>Productos Holísticos para tu Renacer</h2>
    <div class="products">
      <div class="card">
        <h3>Aceites Esenciales Sagrados</h3>
        <p>Mezclas únicas para limpieza energética, protección y conexión espiritual.</p>
      </div>
      <div class="card">
        <h3>Velas de Intención</h3>
        <p>Velitas hechas a mano con hierbas y símbolos para manifestar paz, amor y abundancia.</p>
      </div>
      <div class="card">
        <h3>Cristales Purificadores</h3>
        <p>Amatista, cuarzo rosa y selenita para equilibrar tu espacio y tu energía.</p>
      </div>
      <div class="card">
        <h3>Libros de Meditación Guiada</h3>
        <p>Guías paso a paso para sanar emociones, dormir mejor y conectar con tu alma.</p>
      </div>
    </div>
  </section>

  <!-- Testimonios -->
  <section id="testimonios" class="testimonials">
    <h2>Lo que dicen quienes han renacido</h2>
    <div class="testimonial">
      “Después de mi sesión de limpieza ancestral, sentí como si hubiera soltado un peso que llevaba generaciones cargando. Gracias por ayudarme a volver a respirar.” — Ana M.
    </div>
    <div class="testimonial">
      “Mis espacios ahora respiran paz. Las velas y los cristales que me recomendaste cambiaron la energía de mi hogar.” — Diego R.
    </div>
  </section>

  <!-- Footer -->
  <footer id="contacto">
    <p>🌸 Donde el alma vuelve a florecer. 🌸</p>
    <p>Contáctame para comenzar tu proceso de sanación.</p>
    <p>© 2025 Renacer el Alma — Todos los derechos reservados.</p>
  </footer>

  <script>
    // Animación de pétalos
    function createPetal() {
      const petal = document.createElement("div");
      petal.classList.add("petal");
      petal.style.left = Math.random() * 100 + "vw";
      petal.style.animationDuration = (Math.random() * 5 + 5) + "s";
      petal.style.opacity = Math.random() * 0.5 + 0.3;
      document.body.appendChild(petal);

      setTimeout(() => {
        petal.remove();
      }, 10000);
    }

    setInterval(createPetal, 1000);
  </script>

</body>
</html>

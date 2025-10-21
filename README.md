

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PORTAFOLIO</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <nav class="navbar">
        <div class="logo">
          <img src="Images/Logo.png" alt="MANCAR" class="logo-img" />MANCAR
        </div>
        <ul class="nav-links">
            <li><a href="#home">Inicio</a></li>
            <li><a href="#services">Sobre Mí</a></li>
            <li><a href="#portfolio">Portafolio</a></li>
            <li><a href="#contact">Contacto</a></li>
            <li><a href="#contact" class="cta">Contrátame</a></li>
      </ul>
    </nav>
 </header>  

 <section id="home" class="hero">
    <div class="hero-content">
        <h1 class="hero-title">¡Hola! Soy <span class="highlight">Maicol Carmona</span></h1>
        <p>Diseño experiencias visuales únicas.</p>
        <a href="#portfolio" class="cta">Ver Mi Trabajo</a>
    </div>
 </section>

 <section id="services" class="services">
    <h2>Mis Servicios</h2>
    <div class="service-cards">
        <div class="service-card">
            <h3>Diseño Web</h3>
            <p>Diseños creativos y adaptativos para la web.</p>
        </div>
        <div class="service-card">
            <h3>Creación de marca</h3>
            <p>Creamos tu identidad visual de marca única.</p>
        </div>
        <div class="service-card">
            <h3>Ilustración</h3>
            <p>Ilustraciones originales para todo tipo de proyectos.</p>
        </div>
        <div class="service-card">
            <h3>Modelado 3D</h3>
            <p>Modelados 3D originales para todo tipo de proyectos.</p>
        </div>
    </div>
 </section>
 
 <section id="portfolio" class="portfolio">
    <h2>Mi Portafolio</h2>
    <div class="portfolio-grid">
      <a href="Pagina 2.html">
    <div class="portfolio-item">
      <img src="RENDERS CASA/SALA 2.png" alt="Proyecto 1">
      <div class="portfolio-info">
        <h3>Modelado 3D</h3>
        <p>Modelado de una casa hecha en blender y renderizada en cycles</p>
      </div>
    </div>
    </a>
    <div class="portfolio-grid">
      <a href="pagina 3.html">
    <div class="portfolio-item">
      <img src="DONDE EL SILENCIO GRITA/Portada.jpg" alt="Proyecto 1">
      <div class="portfolio-info">
        <h3>Ilustración</h3>
        <p>Portada de una historia de misterio ilustrada en 2D</p>
      </div>
    </div>
    </a>
  </div>
</section>

 <section id="contact" class="contact">
    <h2>Contacto</h2>
    <form action="https://formsubmit.co/carmonamanjarrezmaicolandres@gmail.com" method="POST">
        <label for=“name"> Nombre </label>
        <input type="text" id="name" name="name" required>
        <label for=“email"> Correo Electrónico </label>
        <input type="email" id="email" name="email" required>
        <label for=“message"> Mensaje </label>
        <textarea id="message" name="message" rows="4" required></textarea>
        <button type="submit" class=“cta"> Enviar Mensaje </button>
    </form>
 </section>
 
 <footer class="footer">
    <div class="footer-content">
        <p>© 2024 [Maicol Carmona] | Todos los derechos reservados</p>
        <div class="social-links">
            <a href="https://www.linkedin.com/in/maicol-carmona-8b8898389?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank">LinkedIn</a>
            <a href="https://www.behance.net/maicolcarmona1" target="_blank">Behance</a>
            <a href="https://www.instagram.com/maicolcarmona13?igsh=bXJsc2dwNW91dzVy" target="_blank">Instagram</a>
        </div>
    </div>
 </footer>
 <script>
  window.history.scrollRestoration = "manual";
 </script>
<div id="custom-cursor" aria-hidden="true"></div>
</body> 
<script>
  const cursor = document.getElementById("custom-cursor");

  let lastX = window.innerWidth / 2;
  let lastY = window.innerHeight / 2;
  let lastTime = performance.now();

  document.addEventListener("mousemove", (e) => {
    const now = performance.now();
    const dt = Math.max(now - lastTime, 8);
    const dx = e.clientX - lastX;
    const dy = e.clientY - lastY;
    const dist = Math.hypot(dx, dy);
    const speed = dist / dt;

    // Estiramiento dinámico según velocidad
    const scaleX = 1 + Math.min(speed * 0.5, 2);
    const scaleY = 1;

    cursor.style.top = `${e.clientY}px`;
    cursor.style.left = `${e.clientX}px`;
    cursor.style.transform = `translate(-50%, -50%) scale(${scaleX}, ${scaleY})`;

    lastX = e.clientX;
    lastY = e.clientY;
    lastTime = now;
  });

  // Ocultar cursor nativo
  document.documentElement.style.cursor = "none";
</script>

</html>
/* ===== RESET ===== */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Arial", sans-serif;
  line-height: 1.6;
  color: #eee;
  background: #0a0a0a;
}

/* ===== NAVBAR ===== */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 5%;
  background: #111;
  color: #fff;
  position: sticky;
  top: 0;
  z-index: 1000;
  box-shadow: 0 2px 8px rgba(255, 0, 0, 0.3);
}

.navbar .logo {
  font-size: 1.5rem;
  font-weight: bold;
}

.logo {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.logo-img {
  width: 32px;
  height: auto;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
}

.nav-links a {
  color: #fff;
  text-decoration: none;
  transition: color 0.3s ease;
}

.nav-links a:hover {
  color: #ff3c3c;
}

.cta {
  background: #ff3c3c;
  padding: 0.35rem 1rem;
  border-radius: 20px;
  transition: 0.3s;
}

.cta:hover {
  background: #cc0000;
  color: #fff;
}

/* ===== HERO ===== */
.hero {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 90vh;
  background-image: url(Images/YO\ MEJOR.png);
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  position: relative;
  color: #fff;
  text-align: center;
  padding: 2rem;
}

.hero h1 .highlight {
  color: #ff3c3c;
}
.hero-title {
  animation: growIn 1.2s ease-out forwards;
  transform-origin: center;
}


/* ===== ABOUT ===== */
.about {
  padding: 3rem 10%;
  text-align: center;
}

.about h2 {
  margin-bottom: 1rem;
  color: #ff3c3c;
}

/* ===== SERVICES ===== */
.services {
  padding: 3rem 10%;
  background: #1a1a1a;
  text-align: center;
}

.service-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
  margin-top: 2rem;
}

.service-card {
  background: #111;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(255, 0, 0, 0.2);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  color: #eee;
}

.service-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 16px rgba(255, 0, 0, 0.4);
}

/* ===== PORTFOLIO ===== */
.portfolio {
  padding: 3rem 10%;
  text-align: center;
}

.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
  margin-top: 2rem;
}

.portfolio-item {
  position: relative;
  overflow: hidden;
  border-radius: 12px;
  box-shadow: 0 4px 8px rgba(255, 0, 0, 0.2);
}

.portfolio-item img {
  width: 100%;
  height: auto;
  display: block;
  transition: transform 0.4s ease;
}

.portfolio-item:hover img {
  transform: scale(1.05);
}

.portfolio-info {
  position: absolute;
  bottom: -100%;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(255, 60, 60, 0.9);
  color: #fff;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  transition: bottom 0.4s ease;
  padding: 1rem;
}

.portfolio-item:hover .portfolio-info {
  bottom: 0;
  opacity: 1;
}

/* ===== CONTACT ===== */
.contact {
  padding: 3rem 10%;
}

.contact form {
  max-width: 600px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.contact input,
.contact textarea {
  width: 100%;
  padding: 0.8rem;
  border: 1px solid #ff3c3c;
  border-radius: 8px;
  font-size: 1rem;
  background: #1a1a1a;
  color: #fff;
}

.contact input:focus,
.contact textarea:focus {
  outline: none;
  border-color: #cc0000;
  box-shadow: 0 0 5px rgba(255, 0, 0, 0.5);
}

.contact button {
  background: #ff3c3c;
  color: #fff;
  border: none;
  padding: 0.8rem;
  border-radius: 20px;
  cursor: pointer;
  transition: 0.3s;
}

.contact button:hover {
  background: #cc0000;
}

/* ===== FOOTER ===== */
.footer {
  background: repeating-linear-gradient(
    45deg,
    rgba(17, 17, 17, 0.9) 0px,
    rgba(17, 17, 17, 0.9) 10px,
    rgba(255, 255, 255, 0.05) 10px,
    rgba(255, 255, 255, 0.05) 20px
  );
  color: #fff;
  padding: 1.5rem;
  text-align: center;
  position: relative;
  z-index: 1;
}


.footer .social-links a {
  margin: 0 0.5rem;
  color: #ff3c3c;
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer .social-links a:hover {
  color: #fff;
}

a {
  text-decoration: none;
}

html {
  scroll-behavior: smooth;
}

h2 {
  text-align: center;
}
/* ===== CURSOR ESTRELLA FUGAZ ===== */
#custom-cursor {
  position: fixed;
  top: 0;
  left: 0;
  width: 20px;
  height: 20px;
  background: radial-gradient(circle, #ff3c3c 0%, #ff0000 80%);
  border-radius: 50%;
  pointer-events: none;
  z-index: 9999;
  transform: translate(-50%, -50%) scale(1, 1);
  transition: transform 0.1s ease-out, background 0.3s ease;
  box-shadow:
    0 0 12px rgba(255, 60, 60, 0.6),
    0 0 24px rgba(255, 0, 0, 0.4),
    0 0 48px rgba(255, 0, 0, 0.2);
}
.hero-content .cta {
  display: inline-block;
  margin-top: 1rem; /* Aumenta este valor si quieres más espacio */
}
@keyframes growIn {
  0% {
    transform: scale(1);
    opacity: 0;
  }
  60% {
    transform: scale(1.1);
    opacity: 1;
  }
  100% {
    transform: scale(1);
  }
}



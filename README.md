

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


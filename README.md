# infografia-el-cartucho
index.html

<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>El Cartucho | Memoria de un territorio</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@500;600;700;800&display=swap');

:root {
  --paper: #eee8dc;
  --paper-light: #f8f5ee;
  --ink: #292722;
  --muted: #777267;
  --red: #824b45;
  --red-dark: #603632;
  --olive: #77765e;
  --line: #c9c0b0;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  scroll-behavior: smooth;
}

body {
  background: var(--paper);
  color: var(--ink);
  font-family: 'DM Sans', sans-serif;
  line-height: 1.65;
}

button {
  font: inherit;
  cursor: pointer;
}

/* NAVEGACIÓN */

.navbar {
  position: sticky;
  top: 0;
  z-index: 100;
  background: rgba(238,232,220,.96);
  border-bottom: 1px solid var(--line);
  padding: 15px 5%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
}

.logo {
  font-family: 'Playfair Display', serif;
  font-weight: 800;
  font-size: 21px;
  letter-spacing: -1px;
}

.logo span {
  color: var(--red);
}

.nav-links {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
}

.nav-links a {
  color: var(--ink);
  text-decoration: none;
  font-size: 12px;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: 600;
}

.nav-links a:hover {
  color: var(--red);
}

/* PORTADA */

.hero {
  min-height: 570px;
  padding: 100px 8%;
  display: grid;
  grid-template-columns: 1.2fr .8fr;
  align-items: center;
  gap: 45px;
  background: var(--paper-light);
  border-bottom: 1px solid var(--line);
}

.eyebrow {
  color: var(--red);
  text-transform: uppercase;
  letter-spacing: 3px;
  font-size: 11px;
  font-weight: 700;
  margin-bottom: 22px;
}

.hero h1 {
  font-family: 'Playfair Display', serif;
  font-size: clamp(55px, 8vw, 105px);
  line-height: .94;
  letter-spacing: -5px;
  margin-bottom: 25px;
}

.hero h1 span {
  color: var(--red);
  display: block;
}

.hero p {
  color: var(--muted);
  max-width: 480px;
  font-size: 16px;
  margin-bottom: 30px;
}

.hero-art {
  min-height: 360px;
  background: var(--red-dark);
  color: var(--paper-light);
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  overflow: hidden;
  padding: 35px;
}

.hero-art::before {
  content: "SANTA INÉS";
  font-family: 'Playfair Display', serif;
  font-size: clamp(35px, 5vw, 70px);
  font-weight: 800;
  opacity: .13;
  position: absolute;
  transform: rotate(-90deg);
  white-space: nowrap;
}

.hero-art-content {
  z-index: 1;
  text-align: center;
}

.hero-art-content strong {
  font-family: 'Playfair Display', serif;
  font-size: 38px;
  display: block;
}

.hero-art-content p {
  color: var(--paper);
  font-size: 12px;
  margin-top: 15px;
}

/* BOTONES */

.btn {
  display: inline-block;
  padding: 13px 22px;
  background: var(--red);
  color: white;
  border: 1px solid var(--red);
  text-decoration: none;
  font-size: 12px;
  letter-spacing: 1px;
  text-transform: uppercase;
  font-weight: 700;
  transition: .25s;
}

.btn:hover {
  background: var(--red-dark);
}

.btn-outline {
  background: transparent;
  color: var(--red);
  margin-left: 8px;
}

/* CONTENIDO */

section {
  padding: 85px 8%;
  border-bottom: 1px solid var(--line);
  scroll-margin-top: 75px;
}

.section-label {
  color: var(--red);
  text-transform: uppercase;
  font-size: 11px;
  letter-spacing: 3px;
  font-weight: 700;
  margin-bottom: 12px;
}

.section-title {
  font-family: 'Playfair Display', serif;
  font-size: clamp(35px, 5vw, 58px);
  line-height: 1.1;
  margin-bottom: 25px;
}

.intro {
  max-width: 730px;
  color: var(--muted);
  font-size: 16px;
  margin-bottom: 45px;
}

.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 18px;
}

.card {
  background: var(--paper-light);
  padding: 28px;
  border: 1px solid var(--line);
  transition: .3s;
}

.card:hover {
  transform: translateY(-5px);
  border-color: var(--red);
}

.card-number {
  font-family: 'Playfair Display', serif;
  font-size: 42px;
  color: var(--red);
  margin-bottom: 15px;
}

.card h3 {
  font-family: 'Playfair Display', serif;
  font-size: 23px;
  margin-bottom: 12px;
}

.card p {
  color: var(--muted);
  font-size: 13px;
}

/* IMAGENES */

.image-placeholder {
  min-height: 230px;
  background: #d8d0c2;
  border: 1px dashed var(--olive);
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 25px;
  color: #625e53;
  font-size: 12px;
  margin-bottom: 22px;
}

/* LINEA DE TIEMPO */

.timeline {
  position: relative;
  max-width: 850px;
  margin: 45px auto 0;
}

.timeline::before {
  content: "";
  position: absolute;
  left: 17px;
  top: 0;
  bottom: 0;
  width: 2px;
  background: var(--red);
}

.timeline-item {
  position: relative;
  padding: 0 0 38px 55px;
}

.timeline-item::before {
  content: "";
  position: absolute;
  left: 9px;
  top: 5px;
  width: 17px;
  height: 17px;
  border-radius: 50%;
  background: var(--red);
  border: 3px solid var(--paper);
}

.timeline-item h3 {
  font-family: 'Playfair Display', serif;
  font-size: 23px;
  margin-bottom: 8px;
}

.timeline-item p {
  color: var(--muted);
  font-size: 14px;
}

/* BLOQUE DESTACADO */

.quote {
  background: var(--red-dark);
  color: var(--paper-light);
  padding: 65px 10%;
  text-align: center;
}

.quote h2 {
  font-family: 'Playfair Display', serif;
  font-size: clamp(30px, 4vw, 47px);
  line-height: 1.2;
  max-width: 850px;
  margin: auto;
}

.quote p {
  color: #ded0c1;
  font-size: 11px;
  margin-top: 20px;
  letter-spacing: 2px;
  text-transform: uppercase;
}

/* INTERACCIÓN */

.interactive {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 12px;
  margin-top: 30px;
}

.interactive button {
  border: 1px solid var(--line);
  background: var(--paper-light);
  color: var(--ink);
  padding: 22px;
  text-align: left;
  transition: .2s;
}

.interactive button:hover,
.interactive button.active {
  background: var(--red);
  color: white;
}

.interactive button strong {
  display: block;
  font-family: 'Playfair Display', serif;
  font-size: 20px;
  margin-bottom: 5px;
}

.detail-panel {
  background: var(--paper-light);
  padding: 30px;
  border-left: 4px solid var(--red);
  margin-top: 15px;
  min-height: 130px;
}

.detail-panel h3 {
  font-family: 'Playfair Display', serif;
  font-size: 25px;
  margin-bottom: 10px;
}

.detail-panel p {
  color: var(--muted);
  font-size: 14px;
}

/* FUENTES */

.source {
  background: #e4ddcf;
  padding: 30px;
  margin-top: 25px;
  font-size: 13px;
  color: var(--muted);
}

.source a {
  color: var(--red);
  overflow-wrap: anywhere;
}

/* PIE */

footer {
  background: var(--ink);
  color: var(--paper);
  padding: 45px 8%;
  text-align: center;
}

footer h2 {
  font-family: 'Playfair Display', serif;
  font-size: 28px;
  margin-bottom: 10px;
}

footer p {
  font-size: 12px;
  color: #c6beaf;
}

/* RESPONSIVE */

@media(max-width: 750px) {
  .navbar {
    align-items: flex-start;
    flex-direction: column;
  }

  .nav-links {
    gap: 12px;
  }

  .nav-links a {
    font-size: 10px;
  }

  .hero {
    grid-template-columns: 1fr;
    padding: 65px 7%;
  }

  .hero h1 {
    letter-spacing: -3px;
  }

  .hero-art {
    min-height: 250px;
  }

  section {
    padding: 65px 7%;
  }

  .grid {
    grid-template-columns: 1fr;
  }

  .interactive {
    grid-template-columns: 1fr;
  }
}
</style>
</head>

<body>

<!-- NAVEGACION -->

<header class="navbar">
  <div class="logo">EL <span>CARTUCHO.</span></div>

  <nav class="nav-links">
    <a href="#inicio">Inicio</a>
    <a href="#origen">Origen</a>
    <a href="#transformacion">Transformación</a>
    <a href="#memoria">Memoria</a>
    <a href="#fuentes">Fuentes</a>
  </nav>
</header>

<!-- PORTADA -->

<main>

<section class="hero" id="inicio">

  <div>
    <div class="eyebrow">Bogotá · Memoria urbana</div>

    <h1>EL <span>CARTUCHO</span></h1>

    <p>
      La historia de un territorio, sus transformaciones
      y las memorias que permanecen en la ciudad.
    </p>

    <a class="btn" href="#origen">Explorar historia</a>
    <a class="btn btn-outline" href="#recorrido">Recorrido</a>
  </div>

  <div class="hero-art">
    <div class="hero-art-content">
      <strong>Un lugar.</strong>
      <strong>Muchas historias.</strong>
      <p>SANTA INÉS · BOGOTÁ</p>
    </div>
  </div>

</section>

<!-- INTRODUCCION -->

<section id="origen">

  <div class="section-label">01 / Contexto histórico</div>

  <h2 class="section-title">
    Antes de llamarse<br>El Cartucho
  </h2>

  <p class="intro">
    Para comprender la historia de El Cartucho es necesario
    acercarse a los antecedentes del territorio de Santa Inés.
    Su historia no comienza con las problemáticas que lo
    hicieron conocido, sino con la memoria de un espacio
    urbano y las transformaciones que experimentó a lo largo
    del tiempo.
  </p>

  <div class="grid">

    <article class="card">
      <div class="card-number">01</div>
      <h3>El territorio</h3>
      <p>
        Explora los antecedentes históricos de Santa Inés
        y su relación con el desarrollo urbano de Bogotá.
      </p>
    </article>

    <article class="card">
      <div class="card-number">02</div>
      <h3>La vida cotidiana</h3>
      <p>
        Una mirada a las viviendas, las actividades y las
        relaciones sociales que construyeron la memoria del sector.
      </p>
    </article>

    <article class="card">
      <div class="card-number">03</div>
      <h3>Los cambios</h3>
      <p>
        Reconoce cómo las transformaciones del entorno
        modificaron las dinámicas del territorio.
      </p>
    </article>

  </div>

</section>

<!-- TRANSFORMACION -->

<section id="transformacion">

  <div class="section-label">02 / Transformaciones</div>

  <h2 class="section-title">
    Un territorio en transformación
  </h2>

  <p class="intro">
    La historia de El Cartucho está relacionada con
    diferentes procesos de transformación urbana y social.
    Para comprenderlos es necesario observar el territorio
    desde sus distintas etapas, sin reducir su historia
    a una sola problemática.
  </p>

  <div class="image-placeholder">
    ESPACIO PARA FOTOGRAFÍA HISTÓRICA DEL SECTOR<br>
    Incorporar únicamente imágenes autorizadas de la publicación.
  </div>

  <div class="grid">

    <article class="card">
      <h3>Transformación social</h3>
      <p>
        Explora los cambios en las condiciones de vida
        y las dinámicas sociales del sector.
      </p>
    </article>

    <article class="card">
      <h3>Transformación urbana</h3>
      <p>
        Observa los cambios en el espacio construido
        y en la relación del sector con la ciudad.
      </p>
    </article>

    <article class="card">
      <h3>Memoria del lugar</h3>
      <p>
        Reconoce las experiencias humanas que forman
        parte de la historia del territorio.
      </p>
    </article>

  </div>

</section>

<!-- RECORRIDO -->

<section id="recorrido">

  <div class="section-label">03 / Recorrido histórico</div>

  <h2 class="section-title">
    Una historia en diferentes momentos
  </h2>

  <p class="intro">
    Selecciona cada etapa para explorar los diferentes
    momentos de la historia del territorio.
    Las fechas y acontecimientos específicos deben
    completarse a partir de la publicación del IDPC.
  </p>

  <div class="timeline">

    <div class="timeline-item">
      <h3>Los antecedentes</h3>
      <p>
        La historia del barrio Santa Inés y la configuración
        de este espacio dentro de Bogotá.
      </p>
    </div>

    <div class="timeline-item">
      <h3>Los cambios del sector</h3>
      <p>
        Las transformaciones urbanas y sociales que
        modificaron las dinámicas del territorio.
      </p>
    </div>

    <div class="timeline-item">
      <h3>El Cartucho</h3>
      <p>
        La consolidación de una realidad social compleja
        que marcó la memoria del sector.
      </p>
    </div>

    <div class="timeline-item">
      <h3>La intervención urbana</h3>
      <p>
        Los procesos de intervención y transformación
        del espacio urbano.
      </p>
    </div>

    <div class="timeline-item">
      <h3>La memoria permanece</h3>
      <p>
        Una reflexión sobre el territorio, sus habitantes
        y las huellas de su historia.
      </p>
    </div>

  </div>

</section>

<!-- BLOQUE EDITORIAL -->

<div class="quote">
  <h2>
    Un lugar puede transformarse,
    pero su historia sigue formando
    parte de la memoria de la ciudad.
  </h2>
  <p>El Cartucho · Memoria urbana</p>
</div>

<!-- INTERACTIVIDAD -->

<section id="memoria">

  <div class="section-label">04 / Explora y descubre</div>

  <h2 class="section-title">
    Conoce las dimensiones de su historia
  </h2>

  <p class="intro">
    La historia de El Cartucho puede comprenderse
    desde diferentes perspectivas. Selecciona una
    para explorar su dimensión.
  </p>

  <div class="interactive">

    <button onclick="showDetail(0,this)">
      <strong>El territorio</strong>
      <span>Espacio y transformación urbana</span>
    </button>

    <button onclick="showDetail(1,this)">
      <strong>Las personas</strong>
      <span>Habitantes y experiencias sociales</span>
    </button>

    <button onclick="showDetail(2,this)">
      <strong>La ciudad</strong>
      <span>Intervención y transformación</span>
    </button>

    <button onclick="showDetail(3,this)">
      <strong>La memoria</strong>
      <span>Historia y patrimonio</span>
    </button>

  </div>

  <div class="detail-panel" id="detail">
    <h3>Selecciona una dimensión</h3>
    <p>
      Haz clic en cualquiera de las opciones para
      descubrir su contenido.
    </p>
  </div>

</section>

<!-- REFLEXION -->

<section>

  <div class="section-label">05 / Reflexión final</div>

  <h2 class="section-title">
    ¿Qué queda después de transformar un lugar?
  </h2>

  <p class="intro">
    La transformación de un territorio no se limita
    a los cambios físicos de sus calles y construcciones.
    También involucra historias personales, relaciones
    sociales, recuerdos y formas de habitar la ciudad.
    Comprender El Cartucho implica reconocer que detrás
    de un espacio urbano existen múltiples experiencias
    que merecen ser documentadas y recordadas.
  </p>

</section>

<!-- FUENTES -->

<section id="fuentes">

  <div class="section-label">06 / Referencias</div>

  <h2 class="section-title">Fuente documental</h2>

  <div class="source">

    <strong>Publicación principal</strong>

    <p>
      Morris, I. (2011).
      <em>En un lugar llamado el Cartucho.</em>
      Instituto Distrital de Patrimonio Cultural.
    </p>

    <p style="margin-top:15px">
      Documento de consulta:
    </p>

    <a href="https://idpc.gov.co/publicaciones/descargas/cartucho.pdf"
       target="_blank" rel="noopener">
      Consultar publicación original del IDPC
    </a>

    <p style="margin-top:20px">
      Esta infografía es un ejercicio académico de
      interpretación y diseño de información basado
      en la publicación indicada.
    </p>

  </div>

</section>

</main>

<footer>
  <h2>EL CARTUCHO</h2>
  <p>Una mirada a la memoria urbana de Bogotá.</p>
  <p style="margin-top:15px">
    Proyecto académico · Periodismo infográfico
  </p>
  <p>Fuente documental: Instituto Distrital de Patrimonio Cultural</p>
</footer>

<script>

const details = [
  {
    title: "El territorio",
    text: "Santa Inés constituye el punto de partida para comprender la historia del sector. Su evolución debe analizarse desde los antecedentes urbanos documentados en la publicación."
  },
  {
    title: "Las personas",
    text: "La dimensión social permite acercarse a las experiencias de quienes habitaron el sector y comprender las diferentes realidades humanas que hicieron parte de su historia."
  },
  {
    title: "La ciudad",
    text: "Las transformaciones urbanas modificaron el espacio y su relación con Bogotá. La intervención debe analizarse considerando tanto sus cambios físicos como sus implicaciones sociales."
  },
  {
    title: "La memoria",
    text: "La memoria permite reconocer que la historia de un lugar no desaparece cuando cambia su paisaje. Los relatos y experiencias forman parte de la identidad urbana."
  }
];

function showDetail(index, button) {

  const panel = document.getElementById("detail");

  panel.innerHTML = `
    <h3>${details[index].title}</h3>
    <p>${details[index].text}</p>
  `;

  document.querySelectorAll(".interactive button")
    .forEach(btn => btn.classList.remove("active"));

  button.classList.add("active");
}

</script>

</body>
</html>

<html lang="de">
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">

  <style>
  <!-- Deine bisherigen Fonts (Beispiel) -->
  <link href="https://fonts.googleapis.com/css2?family=Tangerine:wght@400;700&family=Playfair+Display:wght@700&display=swap" rel="stylesheetische Zeilen -->
  <link href="https://fonts.googleapis.com/css2?family=Gulzar&display=le>
   

    /* Globale Basis: überall Tangerine (außer gezielte Ausnahmen) */
    body {
      margin: 0;
      font-family: 'Tangerine', cursive;
      background: #f8f8f8;
      color: #333;
      line-height: 1.6;
    }

    /* Dezenter Standardabstand */
    p, h1, h2, h3, h4, h5, h6 {
      margin-bottom: 10px;
    }

    /* Abschnitts-Layout + Intro-Animation */
    section {
      padding: 40px 20px;
      max-width: 900px;
      margin: auto;
      opacity: 0;
      transform: translateY(30px);
      animation: fadeIn 1.5s forwards;
    }

    /* Lesbare Größen und Farben */
    h1 { font-size: 56px; color: #444; }
    h2 { font-size: 48px; margin-bottom: 20px; color: #444; }
    h3 { font-size: 22px; color: #333; }
	h4 { font-size: 24px;margin: 6px 0; color: #333; }
	h5 {  text-align: center; font-size: 44px; margin-bottom: 20px;color: #444; }
	h6 { font-size: 30px; margin-bottom: 20px;color: #444; } 
    p  { font-size: 24px; margin: 6px 0; color: #333; }

	  
.details h7 {
  margin: 0;
  font-size: 20px;
  font-family: 'Gulzar', serif;
 

    /* Fade-in on scroll */
    .animate-on-scroll {
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 1.2s ease, transform 1.2s ease;
    }
    .animate-on-scroll.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* HERO */
    .hero {
      height: 100vh;
      background: url('hero.png') center/cover no-repeat;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      color: #fff;
      text-shadow: 0 2px 4px rgba(0,0,0,0.6);
      opacity: 1; 
      transform: none; 
      animation: none; /* Hero selbst nicht animiert */
		position: relative;
    }
	  
/* Sanfter Übergang am unteren Rand des Hero-Bildes */
.hero::after {
  content: "";
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: 120px; /* Übergangshöhe – bei Bedarf anpassen */
  pointer-events: none;
  background: linear-gradient(
    to bottom,
    rgba(248, 248, 248, 0) 0%,
    rgba(248, 248, 248, 0.7) 60%,
    #f8f8f8 100%
  );
}


    .hero h1 { 
      font-size: 64px;
      margin: 0;
      /* bleibt Tangerine über die body-Regel */
    }

    .hero .sub { 
      font-size: 36px; 
      margin: 10px 0; 
      /* bleibt Tangerine über die body-Regel */
    }

    /* Monogramm: Initialen „A ♥ M“ bleiben Playfair Display (Ausnahme) */
    .monogram {
      margin: 60px auto;
      text-align: center;
    }
    .monogram .initials {
      font-family: 'Playfair Display', serif; /* AUSNAHME: nicht Tangerine */
      font-size: 100px;
      font-weight: bold;
      letter-spacing: 10px;
      color: #fff;
    }
    .monogram .symbol {
      font-size: 50px;
      color: #fff;
      margin: 0 10px;
    }
    /* Die Namen darunter nutzen Tangerine (über body), wenn du Parisienne willst, sag Bescheid */
    .monogram .names {
      font-size: 32px;
      margin-top: 10px;
      color: #fff;
    }

    /* Zusätzliche Abstände */
    .extra-space  { display: block; height: 40px; }
    .extra-space1 { display: block; height: 25px; }
    .extra-space2 { display: block; height: 15px; }

    /* Karte */
    .map { width: 100%; border-radius: 8px; margin-top: 16px; }

    /* Keyframes */
    @keyframes fadeIn {
      to { opacity: 1; transform: translateY(0); }
    }

    /* Elegantes Timing-Layout */
    .timing-container { 
      display: flex; 
      flex-direction: column; 
      gap: 20px; 
      border-left: 2px solid #ccc; 
      padding-left: 20px; 
    }
    .event { 
      display: flex; 
      flex-direction: row; 
      align-items: flex-start; 
      gap: 20px; 
    }
    .time { 
      font-size: 26px; 
      font-weight: 700; 
      color: #555; 
      width: 70px; 
      text-align: right; 
    }
    .details { flex: 1; }
    .details h3 { margin: 0; } /* bleibt Tangerine */
    .details p  { margin: 4px 0 0; color: #666; }

    /* Responsive Anpassungen */
    @media (max-width: 600px) {
      .hero h1   { font-size: 50px; }
      .hero .sub { font-size: 28px; }
      h2 { font-size: 40px; }
      h3 { font-size: 22px; }
		h4 { font-size: 26px; }
      p  { font-size: 24px; }
      .time { width: 60px; font-size: 22px; }
    }
  </style>

  <script>
    document.addEventListener('DOMContentLoaded', function() {
      const elements = document.querySelectorAll('.animate-on-scroll');
      const observer = new IntersectionObserver(entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add('visible');
            // Optional: deaktivieren, wenn nur einmal animiert werden soll:
            // observer.unobserve(entry.target);
          }
        });
      }, { threshold: 0.2 });

      elements.forEach(el => observer.observe(el));
    });
  </script>
</head>
<body>

  <!-- Monogramm -->
  <section class="hero">
    <section class="monogram">
      <div class="initials">A<span class="symbol">♥</span>M</div>
      <div class="sub">Save the Date</div>
      <div class="sub">20/03/2026</div>
    </section>
  </section>
	<section class="intro">
		
 <h5 class="animate-on-scroll">Ahmad & Mina</h5>
		<span class="extra-space1"></span>
  </section>
  <section class="intro">
    <span class="extra-space1"></span>
    <h6 class="animate-on-scroll">Liebe Familie und Freunde,</h6>
    <span class="extra-space2"></span>
    <p class="animate-on-scroll"> wir freuen uns sehr, euch zu unserer Hochzeit einzuladen. Dieser besondere Tag findet am <strong>20. März 2026 um 16:00 Uhr</strong> im Ariana Event statt. Wir können es kaum erwarten, diesen einzigartigen Moment mit euch zu teilen.</p>
    <span class="extra-space1"></span>
    <p class="animate-on-scroll">Damit wir besser planen können, bitten wir euch, uns bis Anfang Februar mitzuteilen, ob ihr dabei sein könnt. </p>
    <span class="extra-space1"></span>
    <p class="animate-on-scroll">Sie sind herzlich eingeladen – die Einladung gilt für<strong> 4 Personen</strong>.</p>
	   <span class="extra-space1"></span>
	   <span class="extra-space1"></span>
	  <h7 class="animate-on-scroll"> این یک خط فارسی است که فق .</p>
		  <h7 class="animate-on-scroll"> این یک خط فارسی است که فق .</p>
			  <h7 class="animate-on-scroll"> این یک خط فارسی است که فق .</p>
  </section>
  



  <section class="timing">
    <h2 class="animate-on-scroll">Timing</h2>
    <span class="extra-space"></span>
    <span class="extra-space1"></span>
    <div class="timing-container">
      <div class="event">
        <div class="time">16:00</div>
        <div class="details">
          <h3 class="animate-on-scroll">Einlass &amp; Begrüßung</h3>
          <p class="animate-on-scroll">Die Gäste treffen ein, nehmen Platz.</p>
        </div>
      </div>
      <div class="event">
        <div class="time">17:00</div>
        <div class="details">
          <h3 class="animate-on-scroll">Tanz mit traditioneller Musik</h3>
        </div>
      </div>
      <div class="event">
        <div class="time">18:00</div>
        <div class="details">
          <h3 class="animate-on-scroll">Ankunft des Brautpaars in Gand Afghani</h3>
        </div>
      </div>
      <div class="event">
        <div class="time">19:30</div>
        <div class="details">
          <h3 class="animate-on-scroll">Abendessen</h3>
        </div>
      </div>
      <div class="event">
        <div class="time">21:30</div>
        <div class="details">
          <h3 class="animate-on-scroll">Das Brautpaar im weißen Hochzeitsoutfit</h3>
        </div>
      </div>
      <div class="event">
        <div class="time">22:30</div>
        <div class="details">
          <h3 class="animate-on-scroll">Dance &amp; Party</h3>
        </div>
      </div>
      <div class="event">
        <div class="time">1:00</div>
        <div class="details">
          <h3 class="animate-on-scroll">Schluss</h3>
          <p class="animate-on-scroll">Danke, dass ihr dabei wart – kommt gut nach Hause</p>
        </div>
      </div>
    </div>
  </section>
    <section class="location">
    <h2 class="animate-on-scroll">Location</h2>
		<span class="extra-space1"></span>
	<h3 class="animate-on-scroll">Aria Event</h3>
<h4 class="animate-on-scroll">
        <a href="https://maps.app.goo.gl/VR3mmCs7T4rjWXsy7?g_st=ipc"
           target="_blank"
           rel="noopener noreferrer">
           Christine‑Touaillon‑Straße 4, 1220 Wien
        </a>
    </h4>

    <img src="map.png" alt="Karte zur Location" class="map">
</section>

</body>
</html>


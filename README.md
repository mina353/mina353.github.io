

<html lang="de">
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">

<style>

body {
    font-family: Arial, sans-serif;
    margin: 50px;
}
.animate-on-scroll {
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 1.2s ease, transform 1.2s ease;
}
.animate-on-scroll.visible {
    opacity: 1;
    transform: translateY(0);
}
p, h1, h2, h3, h4, h5, h6 {
    margin-bottom: 10px; /* dezenter Abstand */
}
</style>
<script>
document.addEventListener('DOMContentLoaded', function() {
    const elements = document.querySelectorAll('.animate-on-scroll');
    const observer = new IntersectionObserver(entries => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.classList.add('visible');
            }
        });
    }, { threshold: 0.2 });

    elements.forEach(el => observer.observe(el));
});
</script>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Einladung – Ahmad & Mina</title>
<style>
    body { margin:0; font-family: 'Georgia', serif; background:#f8f8f8; color:#333; line-height:1.6; }
    section { padding: 40px 20px; max-width: 900px; margin: auto; opacity:0; transform: translateY(30px); animation: fadeIn 1.5s forwards; }
	h2 { font-size: 35px; margin-bottom: 20px; color:#444; font-family: 'Pinyon Script', cursive; }
    p  { font-size: 18px; margin: 6px 0; }

    /* HERO */
    .hero {
      height: 100vh;
      background: url('hero.png') center/cover no-repeat;
      display:flex; flex-direction:column; justify-content:center; align-items:center;
      color:#fff; text-shadow:0 2px 4px rgba(0,0,0,0.6);
      opacity:1; transform:none; animation:none;
    }


	
.monogram {
  margin: 60px auto;
  text-align: center;
}

.monogram .initials {
  font-family: 'Playfair Display', serif;
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

.monogram .names {
  font-family: 'Parisienne', cursive;
  font-size: 28px;
  margin-top: 10px;
  color: #fff;
}

	
	 
.extra-space {
    display: block;
    height: 40px; /* erzeugt sichtbaren Abstand */
}
.extra-space1 {
    display: block;
    height: 25px; /* erzeugt sichtbaren Abstand */
}
.extra-space2 {
    display: block;
    height: 15px; /* erzeugt sichtbaren Abstand */
}
    .hero h1 { font-size: 35px; margin:0; font-family: 'Georgia', serif; }
    .hero .sub { font-size: 48px; margin:10px 0; font-family:  'Tangerine', cursive; }

    .intro { animation-delay: 0.5s; }
    .location { animation-delay: 1s; }
    .timing { animation-delay: 1.5s; }

    .map { width:100%; border-radius:8px; margin-top:16px; }

    /* Animation */
    @keyframes fadeIn { to { opacity:1; transform: translateY(0); } }

    /* Elegantes Timing-Layout */
    .timing-container { display:flex; flex-direction:column; gap:20px; border-left:2px solid #ccc; padding-left:20px; }
    .event { display:flex; flex-direction:row; align-items:flex-start; gap:20px; }
    .time { font-size:20px; font-weight:bold; color:#555; width:60px; text-align:right; }
    .details { flex:1; }
    .details h3 { margin:0; font-size:15px; font-family:'Georgia', serif; color:#333; }
    .details p { margin:4px 0 0; font-size:16px; color:#666; }

    @media (max-width:600px){
      .hero h1 { font-size:50px; }
      .hero .sub { font-size:22px; }
      .time { width:50px; font-size:18px; }
    }
</style>
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
    <h2 class="animate-on-scroll">Willkommen!</h2>
	<span class="extra-space1"></span>
    <p class="animate-on-scroll">Liebe Familie und Freunde,</p>
	<span class="extra-space2"></span>
	<p class="animate-on-scroll">wir freuen uns sehr, euch zu unserer Hochzeit einzuladen. Dieser besondere Tag findet am 20. März 2025 um 16:00 Uhr im Ariana Event statt. Wir können es kaum erwarten, diesen einzigartigen Moment mit euch zu teilen.</p>
	<span class="extra-space1"></span>
	<p class="animate-on-scroll">Damit wir besser planen können, bitten wir euch, uns bis Anfang Februar mitzuteilen, ob ihr dabei sein könnt.</p>
	<span class="extra-space1"></span>
	<p class="animate-on-scroll">Sie sind herzlich eingeladen – die Einladung gilt für 4 Personen.</p>
  </section>

  <section class="location">
    <h2 class="animate-on-scroll">Location</h2>
	<span class="extra-space1"></span>
	<h3 class="animate-on-scroll">Aria Event</h3>
<p class="animate-on-scroll">
        Adresse:
        <a href="https://maps.app.goo.gl/VR3mmCs7T4rjWXsy7?g_st=ipc"
           target="_blank"
           rel="noopener noreferrer">
           Christine‑Touaillon‑Straße 4, 1220 Wien
        </a>
    </p>

    <img src="map.png" alt="Karte zur Location" class="map">
</section>
  


  <section class="timing">
    <h2 class="animate-on-scroll">Timing</h2>
	<span class="extra-space"></span>
	<span class="extra-space1"></span>
    <div class="timing-container">
      <div class="event">
        <div class="time">16:00</div>
        <div class="details">
		  <h3 class="animate-on-scroll">Einlass & Begrüßung</h3>
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
          <h3 class="animate-on-scroll">Dance & Party</h3>
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
</body>
</html>

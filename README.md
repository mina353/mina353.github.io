
<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Einladung – Ahmad & Mina</title>

  <!-- Google Fonts: Tangerine for all text, Playfair Display for initials -->
  https://fonts.googleapis.com
  https://fonts.gstatic.com
  https://fonts.googleapis.com/css2?family=Tangerine:wght@400;700&family=Playfair+Display:wght@400;700&display=swap

  <style>
    /* Basis: überall Tangerine, außer wo explizit überschrieben */
    body {
      margin: 0;
      font-family: 'Tangerine', cursive;
      background: #f8f8f8;
      color: #333;
      line-height: 1.6;
    }

    /* Dezenter Abstand für Standardtexte */
    p, h1, h2, h3, h4, h5, h6 {
      margin-bottom: 10px;
    }

    /* Abschnitts-Animation */
    section {
      padding: 40px 20px;
      max-width: 900px;
      margin: auto;
      opacity: 0;
      transform: translateY(30px);
      animation: fadeIn 1.5s forwards;
    }

    /* Überschriften & Fließtext – lesbar skaliert */
    h1 { font-size: 56px; color: #444; }
    h2 { font-size: 48px; margin-bottom: 20px; color: #444; }
    h3 { font-size: 28px; color: #333; }
    p  { font-size: 22px; margin: 6px 0; color: #333; }

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
      opacity: 1; transform: none; animation: none; /* Hero selbst nicht animiert */
    }

    .hero h1 { 
      font-size: 64px; 
      margin: 0; 
      /* bleibt in Tangerine durch body-Regel */
    }

    .hero .sub { 
      font-size: 36px; 
      margin: 10px 0; 
      /* bleibt in Tangerine durch body-Regel */
    }

    /* Monogramm – NUR die Initialen bleiben Playfair Display */
    .monogram {
      margin: 60px auto;
      text-align: center;
    }
    .monogram .initials {
      font-family: 'Playfair Display', serif; /* AUSNAHME: bleibt wie gewünscht */
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
    /* Namen werden jetzt auch in Tangerine angezeigt (durch body),
       falls du sie weiterhin in Parisienne willst, kann ich diese Zeile wieder setzen. */
    .monogram .names {
      font-size: 32px;
      margin-top: 10px;

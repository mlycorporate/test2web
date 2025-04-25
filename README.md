<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sushi Surprise - Restaurant de Luxe</title>
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Open+Sans:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary-color: #BFA06F;
      --text-color: #333333;
      --accent-color: #D3AF75;
      --font-heading: 'Playfair Display', serif;
      --font-body: 'Open Sans', sans-serif;
    }
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: var(--font-body);
      color: var(--text-color);
      background: #FFFFFF;
      line-height: 1.6;
      scroll-behavior: smooth;
    }
    header {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(10px);
      z-index: 100;
      border-bottom: 1px solid #eaeaea;
    }
    nav {
      max-width: 1100px;
      margin: auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem;
    }
    .logo h2 {
      font-family: var(--font-heading);
      font-size: 1.8rem;
      color: var(--primary-color);
    }
    nav ul {
      list-style: none;
      display: flex;
      gap: 1.5rem;
    }
    nav a {
      text-decoration: none;
      font-weight: 600;
      color: var(--text-color);
      position: relative;
    }
    nav a::after {
      content: '';
      height: 2px;
      width: 0;
      background: var(--accent-color);
      position: absolute;
      bottom: -4px;
      left: 0;
      transition: width 0.3s;
    }
    nav a:hover::after {
      width: 100%;
    }
    .hero {
      height: 500px;
      background: url('https://source.unsplash.com/featured/?japanese-food,sushi,restaurant') center/cover no-repeat;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 0 1rem;
    }
    .hero h1 {
      font-family: var(--font-heading);
      font-size: 3rem;
      color: #FFFFFF;
      text-shadow: 2px 2px 10px rgba(0,0,0,0.4);
    }
    .container {
      max-width: 1100px;
      margin: 6rem auto 2rem;
      padding: 0 1rem;
    }
    #menu {
      text-align: center;
    }
    #menu h2 {
      font-family: var(--font-heading);
      font-size: 2.5rem;
      margin-bottom: 1rem;
      color: var(--primary-color);
    }
    .menu-card {
      background: #FFFFFF;
      border: 1px solid #eaeaea;
      border-radius: 12px;
      padding: 2rem;
      margin: 1rem auto;
      max-width: 600px;
      box-shadow: 0 8px 16px rgba(0,0,0,0.05);
      transition: transform 0.3s;
    }
    .menu-card:hover {
      transform: translateY(-5px);
    }
    .menu-card h3 {
      font-family: var(--font-heading);
      font-size: 1.8rem;
      margin-bottom: 0.5rem;
      color: var(--primary-color);
    }
    .menu-card p {
      margin-bottom: 1.2rem;
      font-size: 1rem;
      font-weight: 300;
      color: #555555;
    }
    .menu-card span {
      display: inline-block;
      padding: 0.5rem 1rem;
      font-size: 1.2rem;
      font-weight: 600;
      color: #FFFFFF;
      background: var(--accent-color);
      border-radius: 4px;
    }
    #reservation {
      margin-top: 4rem;
    }
    #reservation h2 {
      font-family: var(--font-heading);
      font-size: 2rem;
      color: var(--primary-color);
      text-align: center;
      margin-bottom: 1.5rem;
    }
    #reservation form {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1rem;
      max-width: 700px;
      margin: auto;
    }
    #reservation form input,
    #reservation form textarea,
    #reservation form button {
      padding: 0.8rem;
      border: 1px solid #eaeaea;
      border-radius: 6px;
      font-family: var(--font-body);
    }
    #reservation form input,
    #reservation form textarea {
      font-size: 1rem;
      color: var(--text-color);
    }
    #reservation form textarea {
      grid-column: span 2;
      resize: vertical;
    }
    #reservation form button {
      grid-column: span 2;
      background: var(--primary-color);
      color: #FFFFFF;
      font-weight: 600;
      border: none;
      cursor: pointer;
      transition: background 0.3s;
    }
    #reservation form button:hover {
      background: #a17e50;
    }
    #contact {
      margin: 4rem 0;
      text-align: center;
    }
    #contact p {
      margin: 0.5rem 0;
      font-weight: 300;
    }
    footer {
      text-align: center;
      padding: 2rem 1rem;
      background: #f8f8f8;
      margin-top: 4rem;
      font-size: 0.9rem;
      color: #777777;
    }
    @media (max-width: 768px) {
      nav ul { display: none; }
      .hero h1 { font-size: 2.2rem; }
      #reservation form { grid-template-columns: 1fr; }
      #reservation form button, #reservation form textarea { grid-column: span 1; }
    }
  </style>
</head>
<body>
  <header>
    <nav>
      <div class="logo"><h2>Sushi Surprise</h2></div>
      <ul>
        <li><a href="#accueil">Accueil</a></li>
        <li><a href="#menu">Menu</a></li>
        <li><a href="#reservation">Réservation</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section id="accueil" class="hero"></section>

  <div class="container">
    <section id="menu">
      <h2>Menu Surprise</h2>
      <div class="menu-card">
        <h3>Expérience Prestige</h3>
        <p>Une sélection exclusive de sushis et créations omakase, imaginée par notre chef étoilé, pour une dégustation d'exception.</p>
        <span>60€ / personne</span>
      </div>
    </section>

    <section id="reservation">
      <h2>Réservez votre table</h2>
      <form action="#" method="POST">
        <input type="text" name="name" placeholder="Nom complet" required>
        <input type="email" name="email" placeholder="Email" required>
        <input type="tel" name="phone" placeholder="Téléphone" required>
        <input type="date" name="date" required>
        <input type="time" name="time" required>
        <input type="number" name="guests" placeholder="Convives" min="1" required>
        <textarea name="requests" rows="4" placeholder="Demandes spéciales (optionnel)"></textarea>
        <button type="submit">Confirmer la réservation</button>
      </form>
    </section>

    <section id="contact">
      <h2>Contact & Adresse</h2>
      <p>13 avenue du Maine, 75015 Paris</p>
      <p><a href="tel:+33123456789">01 23 45 67 89</a> • <a href="mailto:contact@sushisurprise.fr">contact@sushisurprise.fr</a></p>
    </section>
  </div>

  <footer>
    <p>&copy; 2025 Sushi Surprise • Tous droits réservés</p>
  </footer>
</body>
</html>

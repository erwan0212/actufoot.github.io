<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ActuFoot - L'actualité du football en direct</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <header>
        <h1>ActuFoot</h1>
        <nav>
            <ul>
                <li><a href="#hero">Accueil</a></li>
                <li><a href="#actus">Actualités</a></li>
                <li><a href="#download">Téléchargement</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="hero">
        <div class="overlay">
            <h2>Vivez le foot en direct !</h2>
            <p>Résultats, news et matchs en temps réel.</p>
            <a href="lien-de-telechargement.apk" class="btn">Télécharger l'application</a>
        </div>
    </section>

    <section id="actus">
        <h2>⚽ Dernières Actualités ⚽</h2>
        <div id="news-container">
            <!-- Actualités chargées par JS -->
        </div>
    </section>

    <section id="download">
        <h2>📲 Téléchargez l'application</h2>
        <p>Restez informé des dernières actus foot.</p>
        <a href="lien-de-telechargement.apk" class="btn">Télécharger</a>
    </section>

    <section id="contact">
        <h2>📩 Contact</h2>
        <p>Une question ? Contactez-nous à <a href="mailto:contact@actufoot.com">contact@actufoot.com</a></p>
    </section>

    <footer>
        <p>&copy; 2025 ActuFoot - Tous droits réservés.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
/* Import Google Font */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;700&display=swap');

body {
    font-family: 'Poppins', sans-serif;
    margin: 0;
    padding: 0;
    background: #f4f4f4;
    text-align: center;
}

/* Navbar */
header {
    background: #222;
    color: white;
    padding: 10px 0;
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    z-index: 1000;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 15px;
}

nav ul li a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

/* Hero section */
#hero {
    background: url('football.jpg') no-repeat center center/cover;
    height: 80vh;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    text-align: center;
    position: relative;
}

#hero .overlay {
    background: rgba(0, 0, 0, 0.5);
    padding: 50px;
    border-radius: 10px;
}

.btn {
    display: inline-block;
    background: #ff4b2b;
    color: white;
    padding: 12px 25px;
    text-decoration: none;
    font-weight: bold;
    border-radius: 5px;
    transition: 0.3s;
}

.btn:hover {
    background: #ff1b00;
}

/* Sections */
section {
    padding: 60px 20px;
}

#news-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.news-item {
    background: white;
    margin: 10px;
    padding: 20px;
    width: 300px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
}

/* Footer */
footer {
    background: #222;
    color: white;
    padding: 20px;
}
document.addEventListener("DOMContentLoaded", function () {
    const newsContainer = document.getElementById("news-container");

    const news = [
        { title: "🏆 PSG champion d'Europe !", content: "Le PSG s'impose 2-1 en finale contre le Real Madrid." },
        { title: "🚀 Mbappé vers le Real ?", content: "Des rumeurs annoncent un transfert imminent de Mbappé." },
        { title: "🔥 Haaland en feu !", content: "Haaland marque 5 buts en un seul match !" }
    ];

    news.forEach(article => {
        let div = document.createElement("div");
        div.className = "news-item";
        div.innerHTML = `<h3>${article.title}</h3><p>${article.content}</p>`;
        newsContainer.appendChild(div);
    });
});


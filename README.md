# Erwan<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ActuFoot - L'actualité du foot en direct</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <header>
        <h1>ActuFoot</h1>
        <nav>
            <ul>
                <li><a href="#actus">Actualités</a></li>
                <li><a href="#download">Téléchargement</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="hero">
        <h2>Suivez toute l'actualité du football en direct !</h2>
        <p>Téléchargez notre application pour ne rien manquer.</p>
        <a href="lien-de-telechargement.apk" class="btn">Télécharger l'application</a>
    </section>

    <section id="actus">
        <h2>Dernières actualités</h2>
        <div id="news-container">
            <!-- Les actus seront chargées ici en JavaScript -->
        </div>
    </section>

    <section id="download">
        <h2>Télécharger l'application</h2>
        <p>Disponible gratuitement pour Android.</p>
        <a href="lien-de-telechargement.apk" class="btn">Télécharger</a>
    </section>

    <section id="contact">
        <h2>Contact</h2>
        <p>Une question ? Contactez-nous à <a href="mailto:contact@actufoot.com">contact@actufoot.com</a></p>
    </section>

    <footer>
        <p>&copy; 2025 ActuFoot - Tous droits réservés.</p>
    </footer>

    <script src="script.js"></script>
</body>body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background: #f4f4f4;
    text-align: center;
}

header {
    background: #333;
    color: white;
    padding: 10px;
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
}

#hero {
    background: url('football.jpg') no-repeat center center/cover;
    color: white;
    padding: 50px 0;
}

.btn {
    display: inline-block;
    background: red;
    color: white;
    padding: 10px 20px;
    text-decoration: none;
    margin-top: 20px;
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
}
document.addEventListener("DOMContentLoaded", function () {
    const newsContainer = document.getElementById("news-container");

    // Simuler des actualités (tu pourras les récupérer depuis une API plus tard)
    const news = [
        { title: "Victoire du PSG en Ligue des Champions", content: "Le PSG s'impose 3-1 contre le Real Madrid." },
        { title: "Messi de retour au Barça ?", content: "Des rumeurs indiquent un possible retour de Messi au FC Barcelone." },
        { title: "Cristiano Ronaldo marque un triplé", content: "Le portugais continue de briller en Arabie Saoudite." }
    ];

    news.forEach(article => {
        let div = document.createElement("div");
        div.className = "news-item";
        div.innerHTML = `<h3>${article.title}</h3><p>${article.content}</p>`;
        newsContainer.appendChild(div);
    });
});

</html>

index.html
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Chafik Pêche - Matériel de Pêche Professionnel</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            font-family: Arial, sans-serif;
            color: white;
        }
        /* Arrière-plan global avec image de pêche au coucher de soleil */
        body {
            background: url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80') no-repeat center center fixed;
            background-size: cover;
            position: relative;
            min-height: 100vh;
        }
        /* Filtre sombre pour lisibilité */
        body::before {
            content: "";
            position: fixed;
            top: 0; left: 0; right: 0; bottom: 0;
            background-color: rgba(0,0,0,0.55);
            z-index: 0;
        }
        /* Contenu principal par-dessus */
        .content {
            position: relative;
            z-index: 1;
            min-height: 100vh;
            background-color: rgba(0, 77, 64, 0.85); /* Vert foncé semi-transparent */
            box-sizing: border-box;
            padding-bottom: 40px;
        }
        header {
            background-color: transparent;
            text-align: center;
            padding: 25px 10px;
            border-bottom: 2px solid #004d40;
        }
        header h1 {
            margin: 0;
            font-size: 2.8em;
        }
        header p {
            font-size: 1.2em;
            margin: 5px 0 0 0;
            font-weight: 300;
        }
        nav {
            background-color: #00796b;
            text-align: center;
            padding: 10px 0;
        }
        nav a {
            color: white;
            font-weight: bold;
            margin: 0 20px;
            text-decoration: none;
            font-size: 1.1em;
            padding: 6px 12px;
            border-radius: 4px;
            transition: background-color 0.3s ease;
        }
        nav a:hover {
            background-color: #004d40;
        }
        section {
            padding: 50px 15px;
            max-width: 1200px;
            margin: auto;
            box-sizing: border-box;
            color: white;
        }
        #accueil {
            text-align: center;
        }
        #accueil h2 {
            font-size: 2.5em;
            margin-bottom: 15px;
            text-shadow: 2px 2px 6px rgba(0,0,0,0.9);
        }
        #accueil p {
            font-size: 1.3em;
            max-width: 700px;
            margin: auto;
            text-shadow: 1px 1px 4px rgba(0,0,0,0.8);
        }
        #boutique {
            background-color: rgba(255,255,255,0.15);
            border-radius: 8px;
            margin-top: 40px;
        }
        .produit {
            display: inline-block;
            width: 30%;
            margin: 15px 1.5%;
            background-color: rgba(255,255,255,0.85);
            color: #004d40;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.3);
            vertical-align: top;
            text-align: center;
            padding: 15px;
            box-sizing: border-box;
            transition: transform 0.3s ease;
        }
        .produit:hover {
            transform: translateY(-8px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.4);
        }
        .produit img {
            width: 100%;
            height: 180px;
            object-fit: cover;
            border-radius: 6px;
        }
        .produit h3 {
            margin-top: 15px;
            margin-bottom: 8px;
        }
        .produit p {
            font-weight: bold;
            margin-bottom: 15px;
            font-size: 1.1em;
        }
        button {
            background-color: #004d40;
            color: white;
            border: none;
            padding: 12px 20px;
            font-size: 1em;
            cursor: pointer;
            border-radius: 6px;
            transition: background-color 0.3s ease;
        }
        button:hover {
            background-color: #00796b;
        }
        #panier {
            background-color: rgba(255,255,255,0.15);
            padding: 25px;
            border-radius: 8px;
            margin-top: 40px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }
        #panier h2 {
            margin-bottom: 20px;
        }
        #liste-panier {
            list-style: none;
            padding-left: 0;
            margin-bottom: 15px;
        }
        #liste-panier li {
            padding: 6px 8px;
            background-color: rgba(0,77,64,0.1);
            margin-bottom: 8px;
            border-radius: 4px;
            color: white; /* Changé de #004d40 (vert) à white */
            font-weight: 600;
        }
        #total {
            font-size: 1.3em;
            font-weight: bold;
            color: white; /* Changé de #004d40 (vert) à white */
        }
        #contact {
            background-color: rgba(255,255,255,0.15);
            border-radius: 8px;
            max-width: 600px;
            margin: 40px auto 60px;
            padding: 30px;
            color: white;
        }
        #contact h2 {
            text-align: center;
            margin-bottom: 20px;
        }
        #contact p {
            margin: 10px 0;
            font-size: 1.1em;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.5);
        }
        form label {
            font-weight: bold;
            margin-top: 15px;
            display: block;
        }
        form input, form textarea {
            width: 100%;
            padding: 8px;
            margin-top: 6px;
            border: none;
            border-radius: 4px;
            box-sizing: border-box;
            font-size: 1em;
        }
        form textarea {
            resize: vertical;
            height: 100px;
        }
        form button[type="submit"] {
            margin-top: 15px;
            background-color: #004d40;
            color: white;
            font-weight: bold;
            padding: 12px 25px;
            border-radius: 5px;
            border: none;
            cursor: pointer;
        }
        form button[type="submit"]:hover {
            background-color: #00796b;
        }
        footer {
            background-color: #004d40;
            text-align: center;
            padding: 15px;
            color: white;
            font-weight: 300;
        }
        @media (max-width: 900px) {
            .produit {
                width: 46%;
            }
        }
        @media (max-width: 600px) {
            .produit {
                width: 100%;
                margin: 10px 0;
            }
            section {
                padding: 30px 10px;
            }
        }
    </style>
</head>
<body>
    <div class="content">
        <header>
            <h1>Chafik Pêche</h1>
            <p>Matériel de pêche professionnel pour tous les passionnés</p>
        </header>
        <nav>
            <a href="#accueil">Accueil</a>
            <a href="#boutique">Boutique</a>
            <a href="#panier">Panier</a>
            <a href="#contact">Contact</a>
        </nav>

  <section id="accueil">
            <h2>Bienvenue chez Chafik Pêche</h2>
            <p>Découvrez notre boutique en ligne spécialisée dans le matériel de pêche professionnel, alliant qualité, performance et innovation pour tous les passionnés. Que vous soyez débutant ou expert, nous avons ce qu'il vous faut pour vos aventures aquatiques.</p>
        </section>
        <section id="boutique">
            <h2>Notre Boutique</h2>
            <div class="produit">
                <img src="https://prod-static-b.chronocarpe.com/mg/product/4/5/45623e7626e2329dce7ab347ebaefa9a286c88a8_202648amb3.jpg" alt="Moulinet Shimano Ultegra 14000 XSE, modèle professionnel pour la pêche en haute mer" />
                <h3>Moulinet Shimano Ultegra 14000 XSE</h3>
                <p>Prix : 2400 MAD</p>
                <button onclick="ajouterAuPanier('Moulinet Shimano Ultegra 14000 XSE', 2400)">Ajouter au Panier</button>
            </div>
        <div class="produit">
            <img src="https://www.intercyprus.com/cdn/shop/files/S4565330d2c164fc48976540ad407a4d7I.webp?v=1752171412&width=1200" alt="Canne à pêche de 1.8 m, idéale pour les débutants" />
                <h3>Canne à pêche 1.8 m</h3>
                <p>Prix : 100 MAD</p>
                <button onclick="ajouterAuPanier('Canne à pêche 1.8 m', 100)">Ajouter au Panier</button>
            </div>
            <div class="produit">
                <img src="https://pecheaventure.fr/302323-large_default/canne-sakura-horosha-casting-extra-heavy-22m-20-100g.jpg" alt="Canne à pêche de 2.2 m, pour une portée étendue" />
                <h3>Canne à pêche 2.2 m</h3>
                <p>Prix : 120 MAD</p>
                <button onclick="ajouterAuPanier('Canne à pêche 2.2 m', 120)">Ajouter au Panier</button>
            </div>
        </section>
     <section id="panier">
            <h2>Votre Panier</h2>
            <ul id="liste-panier"></ul>
            <p>Total : <span id="total">0</span> MAD</p>
            <button onclick="viderPanier()">Vider le Panier</button>
            <br /><br />
            <button onclick="envoyerCommandeWhatsApp()">Commander via WhatsApp</button>
        </section>
     <section id="contact">
            <h2>Contactez-Nous</h2>
            <p>Email : <a href="mailto:pechechafik@gmail.com" style="color: #a0d8d8;">pechechafik@gmail.com</a></p>
            <p>Téléphone : <a href="tel:+212784268157" style="color: #a0d8d8;">07 84 26 81 57</a></p>
            <p>Adresse : Rue Oualili F'ndeq Chejra Gallerie El Kebdani, Tanger, Maroc</p>
            <p>
                <strong>Suivez-nous :</strong><br />
                <a href="https://www.facebook.com/Chafik Ait Oukhzame(Chafik pêche)" target="_blank" rel="noopener" style="color: #3b5998; text-decoration:none; font-size:1.2em;">
                    &#x1F464; Facebook
                </a>
                &nbsp;&nbsp;&nbsp;
                <a href="https://wa.me/212784268157" target="_blank" rel="noopener" style="color: #25D366; text-decoration:none; font-size:1.2em;">
                    &#x2706; WhatsApp
                </a>
            </p>
        </section>
      <footer>
            <p>&copy; 2024 Chafik Pêche. Tous droits réservés.</p>
        </footer>
    </div>

   <script>
        let panier = JSON.parse(localStorage.getItem('panier')) || [];
        let total = panier.reduce((sum, item) => sum + item.prix, 0);

        function ajouterAuPanier(produit, prix) {
            panier.push({ nom: produit, prix: prix });
            total += prix;
            localStorage.setItem('panier', JSON.stringify(panier));
            mettreAJourPanier();
            alert(`${produit} ajouté au panier !`);
        }

        function mettreAJourPanier() {
            const liste = document.getElementById('liste-panier');
            liste.innerHTML = '';
            panier.forEach(item => {
                const li = document.createElement('li');
                li.textContent = `${item.nom} - ${item.prix} MAD`;
                liste.appendChild(li);
            });
            document.getElementById('total').textContent = total;
        }

        function viderPanier() {
            panier = [];
            total = 0;
            localStorage.removeItem('panier');
            mettreAJourPanier();
        }

        function envoyerCommandeWhatsApp() {
            if (panier.length === 0) {
                alert("Votre panier est vide. Ajoutez des produits avant de commander.");
                return;
            }
            let message = "Bonjour, je souhaite commander :\n";
            panier.forEach(item => {
                message += `- ${item.nom} : ${item.prix} MAD\n`;
            });
            message += `\nTotal : ${total} MAD`;
            const url = `https://wa.me/212784268157?text=${encodeURIComponent(message)}`;
            window.open(url, '_blank');
        }

        // Initialiser le panier au chargement
        mettreAJourPanier();
    </script>
</body>

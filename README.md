<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VIP Bahama Mamas</title>
    <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            background: url(https://cdn.discordapp.com/attachments/1262009326462308424/1332778134377857105/vip-logo-template-design-4d689e7e91040916df14217ef869d470_screen.png) no-repeat center center fixed;
            background-size: cover;
            color: #fff;
        }

        .container {
            max-width: 600px;
            margin: 50px auto;
            padding: 30px;
            background: rgba(0, 0, 0, 0.8);
            border-radius: 15px;
            box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.5);
        }

        h1 {
            font-family: 'Pacifico', cursive;
            text-align: center;
            font-size: 2.5rem;
            color: #ffcc00;
            margin-bottom: 20px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        label {
            font-size: 1rem;
            color: #ffcc00;
            display: block;
            margin-bottom: 8px;
        }

        input, select, textarea, button {
            width: 100%;
            padding: 10px;
            font-size: 1rem;
            border: none;
            border-radius: 5px;
        }

        input, select, textarea {
            background: #fff;
            color: #333;
        }

        button {
            background: #ffcc00;
            color: #000;
            font-weight: bold;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        button:hover {
            background: #ffaa00;
        }

        .price {
            font-size: 1.5rem;
            color: #ffcc00;
            text-align: center;
            margin: 20px 0;
            font-weight: bold;
        }

        .discord-button {
            background-color: #5865F2;
            color: white;
            font-size: 1.2rem;
            margin-top: 20px;
            display: block;
            text-align: center;
            padding: 10px;
            text-decoration: none;
            border-radius: 5px;
            transition: background-color 0.3s;
        }

        footer {
            text-align: center;
            margin-top: 30px;
            color: #fff;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>VIP Bahama Mamas</h1>
    <form id="vip-form">
        <!-- Nom complet -->
        <div class="form-group">
            <label for="name">Nom RP :</label>
            <input type="text" id="name" name="name" placeholder="Entrez votre nom RP" required>
        </div>

        <!-- Age RP -->
        <div class="form-group">
            <label for="age">Âge RP :</label>
            <input type="number" id="age" name="age" placeholder="Entrez votre âge RP" required>
        </div>

        <!-- Profession RP -->
        <div class="form-group">
            <label for="job">Profession RP :</label>
            <input type="text" id="job" name="job" placeholder="Entrez votre profession RP" required>
        </div>

        <!-- Raison pour devenir VIP -->
        <div class="form-group">
            <label for="reason">Raison pour devenir VIP :</label>
            <textarea id="reason" name="reason" placeholder="Expliquez pourquoi vous voulez devenir VIP" required></textarea>
        </div>

        <!-- Mode de paiement (RP) -->
        <div class="form-group">
            <label for="payment">Mode de paiement (RP) :</label>
            <select id="payment" name="payment" required>
                <option value="cash">Cash</option>
                <option value="bank">Banque</option>
                <option value="black_money">Argent sale</option>
            </select>
        </div>

        <!-- Montant -->
        <div class="price">Montant : 15 000 $ (RP)</div>

        <!-- Soumettre -->
        <button type="submit">Valider la demande VIP</button>
    </form>

    <!-- Lien Discord -->
    <a href="https://discord.gg/zYk2PuKu" target="_blank" class="discord-button">Rejoindre le Discord</a>
</div>

<!-- Intégration de EmailJS -->
<script src="https://cdn.emailjs.com/dist/email.min.js"></script>
<script>
    emailjs.init(K8fJqGBgOXXNRcbzn)
 

    document.getElementById('vip-form').addEventListener('submit', function(event) {
        event.preventDefault(); // Empêche la soumission par défaut

        const formData = new FormData(this); // Récupère les données du formulaire

        // Envoi des données avec EmailJS
        emailjs.sendForm('service_nh23r52', 'template_u27fcxf', formData)
            .then(function(response) {
                alert('Demande envoyée avec succès');
            }, function(error) {
                alert('Erreur lors de l\'envoi');
            });
    });
</script>

</body>
</html>

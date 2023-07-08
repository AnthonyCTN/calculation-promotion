# calculation-promotion
a site where you put the price and the promotion in % and it displays the final price



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

    <nav>
        <ul>
            <li><a href="application.html">Accueil</a></li>
            <li><a href="asitepresentation.html">Exercice</a></li>
        </ul>
    </nav>

    <div class="container">
        <h1>Calcul de pourcentage</h1>
        <div class="input-group">
          <label for="price">Prix :</label>
          <input type="number" id="price" placeholder="Entrez le prix">
        </div>
        <div class="input-group">
          <label for="percentage">Pourcentage :</label>
          <input type="number" id="percentage" placeholder="Entrez le pourcentage">
        </div>
        <button onclick="calculatePercentage()">Calculer</button>
        <div id="result" class="result-container"></div>
      </div>
      <script >
        function calculatePercentage() {
  var price = parseFloat(document.getElementById('price').value);
  var percentage = parseFloat(document.getElementById('percentage').value);

  if (isNaN(price) || isNaN(percentage)) {
    document.getElementById('result').textContent = 'Veuillez entrer des valeurs valides.';
  } else {
    var result = price - (price * percentage / 100);
    document.getElementById('result').textContent = 'Le résultat final est : ' + result.toFixed(2);
  }
}

      </script>

    
</body>
</html>
<style>
    body {
        font-family: Arial, sans-serif;
        background-color: #292f3f;
        padding: 50px;
    }

    .container {
        background-color: #fff;
        padding: 30px;
        border-radius: 10px;
        box-shadow: 0px 0px 10px 0px rgba(0,0,0,0.1);
        max-width: 500px;
        margin: auto;
    }

    h1 {
        color: #333;
        font-size: 24px;
        text-align: center;
        margin-bottom: 30px;
    }

    .input-group {
        display: flex;
        flex-direction: column;
        margin-bottom: 20px;
    }

    label {
        font-weight: bold;
        color: #666;
        margin-bottom: 10px;
    }

    input {
        padding: 10px;
        border: 1px solid #ddd;
        border-radius: 5px;
        font-size: 16px;
    }

    button {
        padding: 10px;
        background-color: #007BFF;
        color: white;
        border: none;
        border-radius: 5px;
        font-size: 16px;
        cursor: pointer;
        margin-top: 20px;
        transition: background-color 0.3s ease;
    }

    button:hover {
        background-color: #0056b3;
    }

    .result-container {
        margin-top: 20px;
        font-size: 20px;
        color: #333;
        font-weight: bold;
        text-align: center;
    }

nav {
            background-color: #292f3f;
            padding: 10px;
          
        }

        nav ul {
            list-style-type: none;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
        }

        nav li {
            margin: 0 10px;
        }

        nav a {
            color: #fff;
            text-decoration: none;
            font-size: 18px;
        }

        nav a:hover {
            color: #007bff;
        }
</style>

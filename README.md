<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Întrebare V-day</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
            transition: background 0.5s;
        }
        #container {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        button {
            margin: 10px;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        #da {
            background-color: green;
            color: white;
        }
        #nu {
            background-color: red;
            color: white;
        }
        #imagine {
            display: none;
            margin-top: 20px;
            width: 300px;
            height: auto;
        }
    </style>
</head>
<body>

    <div id="container">
        <h2>Vrei să fii partenera mea de V-day?</h2>
        
        <button id="da" onclick="acceptat()">Da</button>
        <button id="nu" onclick="respingere()">Nu</button>

        <img id="imagine" src="" alt="Poza ta" />
    </div>

    <script>
        let marimeDa = 16;

        function respingere() {
            marimeDa += 5; // Crește dimensiunea butonului "Da"
            document.getElementById("da").style.fontSize = marimeDa + "px";
            document.getElementById("da").style.padding = (marimeDa / 2) + "px " + (marimeDa) + "px";
        }

        function acceptat() {
            document.body.style.backgroundColor = "white"; // Schimbă fundalul în alb
            let img = document.getElementById("imagine");
            img.src = "URL_POZA_TA"; // Înlocuiește cu un link către poza dorită
            img.style.display = "block";
        }
    </script>

</body>
</html>

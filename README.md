<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DW GUI KEY</title>
    <style>
        body { margin: 0; display: flex; justify-content: center; align-items: center; height: 100vh; background-color: #f0f0f0; font-family: sans-serif; }
        .card { width: 350px; height: 550px; border: 4px solid black; border-radius: 20px; overflow: hidden; position: relative; }
        
        .page { width: 100%; height: 100%; display: none; flex-direction: column; align-items: center; justify-content: center; text-align: center; }
        .active { display: flex; }

        /* PÁGINA 1: START */
        #p1 { background: linear-gradient(#87CEEB, #32CD32, #FF4500); }
        .btn-start { width: 140px; height: 140px; border-radius: 50%; border: 4px solid black; background: #CCFFCC; font-size: 22px; font-weight: bold; cursor: pointer; }

        /* PÁGINA 2: ESPERA */
        #p2 { background: #87CEEB; color: black; }
        .wait-box { background: white; padding: 20px; border-radius: 15px; border: 3px solid black; margin-top: 20px; font-weight: bold; font-size: 25px; }

        /* PÁGINA 3: COPY */
        #p3 { background: #FFFF33; }
        .key-box { background: white; width: 85%; padding: 15px 0; border: 3px solid black; margin: 30px 0; font-weight: bold; font-size: 16px; }
        .btn-copy { background: #00FF00; color: white; padding: 15px 40px; border-radius: 30px; border: 3px solid black; font-size: 24px; font-weight: bold; cursor: pointer; }
    </style>
</head>
<body>

    <div class="card">
        <div id="p1" class="page active">
            <h1 style="margin-bottom: 50px;">DW GUI KEY<br>THE BEST HUB</h1>
            <button class="btn-start" onclick="goToP2()">^ ^<br>v<br>START</button>
        </div>

        <div id="p2" class="page">
            <h2 style="font-size: 35px;">GENERATING KEY</h2>
            <p style="font-size: 20px;">WAIT 7s</p>
            <div class="wait-box">GENERATE</div>
        </div>

        <div id="p3" class="page">
            <div style="font-size: 60px;">⏱️</div>
            <h2 style="color: white; -webkit-text-stroke: 1.5px black; font-size: 30px;">KEY GENERATED</h2>
            <div class="key-box">DW_5978_THE_BEST_HUB_:3</div>
            <button id="copyBtn" class="btn-copy" onclick="copyAction()">COPY</button>
        </div>
    </div>

    <script>
        // De Página 1 a Página 2
        function goToP2() {
            document.getElementById('p1').classList.remove('active');
            document.getElementById('p2').classList.add('active');
            
            // Cambio automático a Página 3 después de 7 segundos
            setTimeout(() => {
                document.getElementById('p2').classList.remove('active');
                document.getElementById('p3').classList.add('active');
            }, 7000);
        }

        // Acción final en Página 3
        function copyAction() {
            const key = "DW_5978_THE_BEST_HUB_:3";
            const btn = document.getElementById('copyBtn');
            
            navigator.clipboard.writeText(key).then(() => {
                btn.innerText = "★COPIED★";
                btn.style.background = "#00CCFF";
            });
        }
    </script>
</body>
</html>

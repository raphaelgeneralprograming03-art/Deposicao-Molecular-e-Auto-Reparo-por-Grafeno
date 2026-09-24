<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>SROS - Auto-Reparo Quântico</title>
    <style>
        body { background: #050505; color: #e5e5e5; font-family: monospace; display: flex; justify-content: center; align-items: center; min-height: 100vh; margin:0; }
        .hud { border: 2px solid #ffd700; background: rgba(25, 20, 0, 0.8); padding: 25px; width: 420px; border-radius: 8px; box-shadow: 0 0 20px rgba(255, 215, 0, 0.2); }
        h2 { color: #ffd700; text-align: center; border-bottom: 1px solid #ffd700; padding-bottom: 8px; }
        .armor-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 5px; margin: 15px 0; }
        .grid-block { height: 40px; background: #222; border: 1px solid #444; border-radius: 4px; display: flex; align-items: center; justify-content: center; font-size: 0.8em; }
        .damaged { background: #7f0000; border-color: #ff0000; color: #ff9999; animation: blink 1s infinite; }
        @keyframes blink { 50% { opacity: 0.5; } }
        .btn { width: 100%; padding: 12px; background: transparent; border: 2px solid #ffd700; color: #ffd700; font-weight: bold; cursor: pointer; }
        .btn:hover { background: #ffd700; color: #000; }
    </style>
</head>
<body>
    <div class="hud">
        <h2>SROS // MOLECULAR_RECONSTRUCT</h2>
        <div style="font-size: 0.9em; margin-bottom: 5px;">Matriz Estrutural de Grafeno:</div>
        <div class="armor-grid">
            <div class="grid-block">OK</div><div class="grid-block">OK</div><div class="grid-block damaged" id="b1">FALHA</div><div class="grid-block">OK</div>
            <div class="grid-block">OK</div><div class="grid-block damaged" id="b2">FALHA</div><div class="grid-block">OK</div><div class="grid-block">OK</div>
        </div>
        <div style="margin-bottom: 15px; font-size: 0.9em;">Reserva Carbono Metatábico: <span id="c-res" style="color: #ffd700;">100%</span></div>
        <button class="btn" onclick="iniciarReparo()">Injetar Hibridização sp²</button>
    </div>

    <script>
        function iniciarReparo() {
            const b1 = document.getElementById('b1');
            const b2 = document.getElementById('b2');
            const cRes = document.getElementById('c-res');

            setTimeout(() => {
                b1.className = "grid-block"; b1.innerText = "OK";
                cRes.innerText = "95.8%";
            }, 600);

            setTimeout(() => {
                b2.className = "grid-block"; b2.innerText = "OK";
                cRes.innerText = "91.6%";
            }, 1200);
        }
    </script>
</body>
</html>

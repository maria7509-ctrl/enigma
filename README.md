<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Enigma do Galo de Ouro</title>
    <style>
        body {
            background-color: #0b1a2b;
            color: #f5d76e;
            font-family: 'Georgia', serif;
            text-align: center;
            margin-top: 100px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        h1 { font-size: 2.5em; text-shadow: 2px 2px #000; }

        input {
            padding: 12px;
            font-size: 18px;
            text-align: center;
            border-radius: 8px;
            border: 2px solid #f5d76e;
            background: #1a2a3a;
            color: white;
            outline: none;
            transition: 0.3s;
        }

        input:focus { box-shadow: 0 0 10px #f5d76e; }

        button {
            padding: 10px 25px;
            font-size: 16px;
            margin-top: 15px;
            cursor: pointer;
            background-color: #f5d76e;
            color: #0b1a2b;
            border: none;
            border-radius: 5px;
            font-weight: bold;
            transition: 0.2s;
        }

        button:hover {
            background-color: #fff;
            transform: scale(1.05);
        }

        #resultado {
            margin-top: 30px;
            font-size: 1.2em;
            max-width: 500px;
            line-height: 1.6;
        }
    </style>
</head>
<body>

    <h1>🔐 Cofre do Capitão</h1>
    <p>Digite a sequência correta para continuar</p>

    <input type="text" id="senha" placeholder="5-7-3" onkeypress="verificarTecla(event)">
    <br>
    <button onclick="verificarSenha()">Desbloquear</button>

    <p id="resultado"></p>

    <script>
        function verificarSenha() {
            // .trim() remove espaços acidentais antes ou depois da senha
            var senha = document.getElementById("senha").value.trim();
            var campoResultado = document.getElementById("resultado");

            if (senha === "5-7-3") {
                campoResultado.innerHTML = "🌊 Se chegaram até aqui, provaram ser navegadores dignos.<br><br>" +
                "Mas o Galo de Ouro só aparece para aqueles que conseguem ler os sinais do mar.";
                campoResultado.style.color = "#4CAF50"; // Muda para verde no sucesso
            } else {
                campoResultado.innerHTML = "❌ Sequência incorreta... o mar ainda esconde seus segredos.";
                campoResultado.style.color = "#ff4c4c"; // Muda para vermelho no erro
            }
        }

        // Função para detectar a tecla Enter
        function verificarTecla(event) {
            if (event.key === "Enter") {
                verificarSenha();
            }
        }
    </script>

</body>
</html>

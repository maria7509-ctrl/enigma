HTML
<!DOCTYPE html>
<html>
<head>
  <title>Enigma do Galo de Ouro</title>

  <style>
    body {
      background-color: #0b1a2b;
      color: #f5d76e;
      font-family: Georgia, serif;
      text-align: center;
      margin-top: 100px;
    }

    input {
      padding: 10px;
      font-size: 18px;
      text-align: center;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      margin-top: 10px;
      cursor: pointer;
    }
  </style>

  <script>
    function verificarSenha() {
      var senha = document.getElementById("senha").value;

      if (senha === 5-7-3) {
        document.getElementById("resultado").innerHTML =
        🌊 Se chegaram até aqui, provaram ser navegadores dignos.
        Mas o Galo de Ouro só aparece para aqueles que conseguem ler os sinais do mar.
      } else {
        document.getElementById("resultado").innerHTML =
        "❌ Sequência incorreta... o mar ainda esconde seus segredos.";
      }
    }
  </script>

</head>

<body>

<h1>🔐 Cofre do Capitão
<p>Digite a sequência correta para continuar</p>

<input type="text" id="senha" placeholder="Ex: 1-2-3">
<br>
<button onclick="verificarSenha()">Desbloquear</button>

<p id="resultado"></p>

</body>

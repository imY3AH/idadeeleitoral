<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Verificação de Idade</title>
    <style>
        body {
            background-color: rgba(99, 99, 231, 0.514);
            color: white;
            font: normal 30pt arial;
        }
    </style>
</head>

<body>

    <h1>Verificação de idade eleitoral</h1>
  Sua idade <input type="number" name="nidade" id="nidade">
  <input type="button" value="verificar" onclick="observar()">
  <div id="resu"></div>
  
  <script>
    var nome = String(window.prompt("Digite seu nome:"));
    window.alert("Seja bem vindo ao nosso site, " + nome + "!");
    
    function observar() {
      var suaidade = window.document.getElementById('nidade');
      var idade = Number(suaidade.value);
      var resu = window.document.querySelector("div#resu");
      
      resu.innerHTML = `<p>Você tem ${idade} anos.</p>`;
      if (idade < 16) {
        resu.innerHTML = `<p>Você não tem o direito de votar.</p>`;
      } if (idade < 18) {
        resu.innerHTML = `<p>Você pode votar, mas não é obrigatório.</p>`;
      } if (idade >= 18) {
          resu.innerHTML = `<p>Você deve votar!</p>`;
      } if (idade >= 65) {
        resu.innerHTML = `<p>Você pode votar, mas não é obrigatório.</p>`;
      }
    }
  </script>
    
</body>
</html>

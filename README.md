<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Encriptador y Decodificador</title>
   <style>
   body {
      font-family: Cursive ;
      background-color:#f2f2f2;
      display:10px;
      justify-content: center;
      align-items: scenter;
      height: 100vh;
      margin: 0;
    }
 .container {
      background-color: #f1f1f1  ;
      padding: 10px;
      border-radius: 10px;
      box-shadow: 0 0px 8px rgba(0, 0, 0, 0.2);
      text-align: center;
      max-width: 400px;
      width: 100%;
    }
  h1 {
     color: #333;
      margin-bottom: 20px }
 textarea {
      width: 100%;
      height: 100px;
      border: 2px solid #333;
      border-radius: 5px;
      padding: 10px;
      font-size: 16px;
      margin-bottom: 20px;
    }
  button {
      background-color: #3399ff;
      border: none;
      color: white;
      padding: 10px 20px;
      border-radius: 5px;
      font-size: 18px;
      cursor: pointer;
      margin: 5px;
    }
   button:hover {
      background-color: #2877b5;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Encriptador y Decodificador</h1>
    <textarea id="texto" placeholder="Escribe tu texto aquí..."></textarea>
    <br>
    <button onclick="encriptar()">Encriptar</button>
    <button onclick="decodificar()">Decodificar</button>
    <button onclick="copiarTexto()">Copiar</button>
  </div>

  <script>
    function encriptar() {
      let texto = document.getElementById('texto').value;
      texto = texto.replace(/i/gi, 'imes');
      texto = texto.replace(/a/gi, 'ai');
      texto = texto.replace(/o/gi, 'ober');
      texto = texto.replace(/u/gi, 'ufat');
      document.getElementById('texto').value = texto;
    }

    function decodificar() {
      let texto = document.getElementById('texto').value;
      texto = texto.replace(/imes/gi, 'i'); to 
      texto = texto.replace(/ai/gi, 'a');
      texto = texto.replace(/ober/gi, 'o');
      texto = texto.replace(/ufat/gi, 'u');
      document.getElementById('texto').value = texto;
    }

    function copiarTexto() {
      const texto = document.getElementById('texto');
      texto.select();
      texto.setSelectionRange(0, 99999); // Para dispositivos móviles
      document.execCommand('copy');
      alert('Texto copiado al portapapeles');
    }
  </script>
</body>
</html>

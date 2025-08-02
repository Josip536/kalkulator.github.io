<html lang="hr">
<head>
  <meta charset="UTF-8">
  <title>Kalkulator</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 40px; }
    .calc { max-width: 300px; margin: auto; padding: 20px; border: 1px solid #ccc; border-radius: 8px; }
    input, select, button { margin: 8px 0; width: 100%; padding: 8px; box-sizing: border-box; }
    .result { font-size: 1.2em; margin-top: 16px; }
  </style>
</head>
<body>
  <div class="calc">
    <h2>Kalkulator</h2>
    <input type="number" id="num1" placeholder="Prvi broj">
    <select id="op">
      <option value="plus">+</option>
      <option value="minus">-</option>
      <option value="puta">&times;</option>
      <option value="podijeljeno">÷</option>
    </select>
    <input type="number" id="num2" placeholder="Drugi broj">
    <button onclick="izracunaj()">Izračunaj</button>
    <div class="result" id="rezultat"></div>
  </div>
  <script>
    function izracunaj() {
      const a = parseFloat(document.getElementById('num1').value);
      const b = parseFloat(document.getElementById('num2').value);
      const op = document.getElementById('op').value;
      let rez;
      if (isNaN(a) || isNaN(b)) {
        rez = "Unesi oba broja!";
      } else {
        switch(op) {
          case "plus": rez = a + b; break;
          case "minus": rez = a - b; break;
          case "puta": rez = a * b; break;
          case "podijeljeno": 
            if (b === 0) rez = "Dijeljenje s 0 nije dozvoljeno!";
            else rez = a / b;
            break;
        }
      }
      document.getElementById('rezultat').textContent = "Rezultat: " + rez;
    }
  </script>
</body>
</html>

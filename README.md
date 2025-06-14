<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>S4 Average Calculator</title>
  <style>
    body { font-family: Arial; max-width: 600px; margin: auto; padding: 20px; }
    input { margin: 5px 0; padding: 5px; width: 100%; }
    button { padding: 10px 15px; margin-top: 10px; }
    .result { margin-top: 20px; font-size: 1.2em; font-weight: bold; }
  </style>
</head>
<body>
  <h2>S4 Average Calculator</h2>
  <form id="notesForm">
    <label>Methode numerique exam:</label><input type="number" step="0.01" id="a" required />
    <label>Methode numerique TD:</label><input type="number" step="0.01" id="b" required />
    <label>Électronique exam:</label><input type="number" step="0.01" id="c" required />
    <label>Électronique TD:</label><input type="number" step="0.01" id="d" required />
    <label>Électronique TP:</label><input type="number" step="0.01" id="e" required />
    <label>ÉLECTROTECHNIQUE exam:</label><input type="number" step="0.01" id="f" required />
    <label>ÉLECTROTECHNIQUE TD:</label><input type="number" step="0.01" id="g" required />
    <label>ÉLECTROTECHNIQUE TP:</label><input type="number" step="0.01" id="h" required />
    <label>Logique programme et automatise exam :</label><input type="number" step="0.01" id="i" required />
    <label>Logique programme et automatise TD:</label><input type="number" step="0.01" id="j" required />
    <label>Logique programme et automatise TP:</label><input type="number" step="0.01" id="k" required />
    <label>Théorie du signal exam :</label><input type="number" step="0.01" id="l" required />
    <label>Théorie du signal TD:</label><input type="number" step="0.01" id="m" required />
    <label>Mesure electrique:</label><input type="number" step="0.01" id="n" required />
    <label>Téchnique d'expression TD:</label><input type="number" step="0.01" id="o" required />
     <label>Téchnique d'expression  exam:</label><input type="number" step="0.01" id="p" required />
      <label>Dispositifs electrique exam:</label><input type="number" step="0.01" id="q" required />
    <button type="submit">Calculate Average</button>
  </form>
  <div class="result" id="result"></div>

  <script>
    document.getElementById("notesForm").onsubmit = function(e) {
      e.preventDefault();
      const v = id => parseFloat(document.getElementById(id).value) || 0;
      const moyenne = (
        ((v("a")*0.6 + v("b")*0.4)*2 +
         (v("c")*0.6 + v("d")*0.2 +v("e")*0.2)*4 +
         (v("f")*0.6 + v("g")*0.2 +v("h")*0.2)*4 + 
         (v("i")*0.6 + v("j")*0.2 +v("k")*0.2)*4 +
         (v("l")*0.6 + v("m")*0.4)*2 +
         (v("p")*0.6 + v("o")*0.4)*1 +
         v("q")+ v("n")
        ) / 19
      ).toFixed(2);
      document.getElementById("result").innerText = "Your  average is: " + moyenne;
    };
  </script>
</body>
</html>

D'acord, entenc que vols que et proporcioni un esquelet bàsic d'HTML, CSS i JavaScript per començar a construir la teva calculadora d'estalvi energètic. Aquest serà un punt de partida senzill, que podràs anar ampliant i personalitzant.

**index.html (Estructura HTML)**

```html
<!DOCTYPE html>
<html lang="ca">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora Estalvi Energètic</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Calculadora Estalvi Energètic</h1>
        <p>Eina per visualitzar l'impacte de mesures d'estalvi.</p>
    </header>

    <main>
        <section id="introduccio">
            <h2>Introducció</h2>
            <p>Benvingut a la calculadora d'estalvi energètic. Aquesta eina et permetrà estimar l'impacte de diferents mesures d'estalvi al teu centre.</p>
        </section>

        <section id="calculadora">
            <h2>Calculadora</h2>
            <div id="calculs">
                <!-- Aquí aniran els diferents càlculs -->
                <h3>Càlcul 1: Consum elèctric del pròxim any</h3>
                <label for="consum_actual">Consum elèctric actual (kWh/any):</label>
                <input type="number" id="consum_actual" value="117040.67"><br><br>
                <label for="percentatge_estalvi">Percentatge d'estalvi esperat:</label>
                <input type="number" id="percentatge_estalvi" value="10">%<br><br>
                <button onclick="calculaEstalvi()">Calcula l'estalvi</button>
                <p id="resultat"></p>
            </div>
        </section>

        <section id="consells">
            <h2>Consells per Reduir el Consum</h2>
            <ul>
                <li><strong>Electricitat:</strong> Utilitza bombetes LED, apaga els llums quan surtis d'una habitació, optimitza l'ús de la climatització.</li>
                <li><strong>Aigua:</strong> Repara les fuites, utilitza sistemes de descàrrega eficients, rega les plantes a les hores de menys calor.</li>
                <li><strong>Consumibles:</strong> Redueix l'ús de paper, utilitza productes de neteja ecològics, recicla.</li>
            </ul>
        </section>
    </main>

    <footer>
        <p>Creat per [El teu Nom]</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
```

**style.css (Estils CSS)**

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    color: #333;
}

header {
    background-color: #333;
    color: #fff;
    padding: 1em 0;
    text-align: center;
}

main {
    padding: 20px;
}

section {
    margin-bottom: 20px;
    background-color: #fff;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
}

#calculadora input[type="number"] {
    width: 100px;
    padding: 5px;
    border: 1px solid #ccc;
    border-radius: 4px;
}

#calculadora button {
    background-color: #5cb85c;
    color: white;
    padding: 10px 15px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

#consells ul {
    list-style: disc;
    margin-left: 20px;
}

footer {
    text-align: center;
    padding: 1em 0;
    background-color: #333;
    color: #fff;
}
```

**script.js (Lògica JavaScript)**

```javascript
function calculaEstalvi() {
    let consumActual = parseFloat(document.getElementById("consum_actual").value);
    let percentatgeEstalvi = parseFloat(document.getElementById("percentatge_estalvi").value);

    let estalvi = consumActual * (percentatgeEstalvi / 100);
    let consumNou = consumActual - estalvi;

    document.getElementById("resultat").innerText = "Estalvi estimat: " + estalvi.toFixed(2) + " kWh/any. Nou consum estimat: " + consumNou.toFixed(2) + " kWh/any.";
}
```

**Com utilitzar aquest codi:**

1.  **Crea tres fitxers:** Guarda el codi HTML com a `index.html`, el codi CSS com a `style.css` i el codi JavaScript com a `script.js`. Assegura't que estiguin al mateix directori.
2.  **Obre `index.html` al teu navegador:** Això mostrarà la pàgina web amb la calculadora bàsica.
3.  **Modifica els fitxers:** Pots afegir més elements HTML, estils CSS i funcions JavaScript per ampliar la funcionalitat de la calculadora.
4.  **Enllaça el fitxer js al html:** Aquest pas es crucial per tal que tot funcioni.

**Explicació del codi:**

*   **HTML:** Defineix l'estructura de la pàgina web, amb un encapçalament, una secció principal amb la calculadora i els consells, i un peu de pàgina.
*   **CSS:** Defineix l'aparença visual de la pàgina, com els colors, les fonts i la disposició dels elements.
*   **JavaScript:** Conté la lògica per realitzar els càlculs i mostrar els resultats. En aquest exemple, només hi ha una funció que calcula l'estalvi d'energia basat en el consum actual i el percentatge d'estalvi.

Aquest és només un punt de partida. Pots afegir més càlculs, millorar la interfície d'usuari i afegir funcionalitats més avançades a la teva calculadora d'estalvi energètic. Recorda fer servir les dades del fitxer CSV que m'has proporcionat per alimentar els càlculs i oferir una informació més precisa.

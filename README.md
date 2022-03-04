#Stappenplan project opzetten

1. NPM initialiseren `npm init`
2. Parcel installeren `npm i parcel --save-dev`
3. Parcel plugin Nuke Distribution installeren `npm i parcel-plugin-nuke-dist --save-dev`
4. Aanmaken src map
5. Aanmaken index.html in src map
6. Aanmaken styles.css in src map
7. Koppelen styles.css in de head section `<link rel="stylesheet" href="./styles.css"/>`
8. Aanmaken main.js in src map
9. Koppelen main.js boven het sluiten van de body tag `<script src="./main.js" type="module"></script>`
10. Script tag vervangen in package.json `"scripts": {
    "start": "parcel src/index.html",
    "build": "parcel build src/index.html"
    },`
11. Test of alle koppelingen (js en css) en packages (parcel) werken! `npm run start`

#Stappenplan data fetchen
1. Axios installeren `npm i axios`
2. Axios importeren in JS bestand `import axios from "axios";`
3. Asynchrone functie schrijven `async function functionName() { }`
4. Functie aanroepen `functionName()`
5. Functie testen
6. Try & catch block plaatsen in de functie declaratie `try {} catch ( e ) {
   console.error( e ); }`
7. In het try block een request (get/post/put/del) maken naar een endpoint en wachten op antwoord. Deze slaan we op in een variabele. `const response = await axios.get('https://api.uri-here.org/endpoint')`
8. Test response
9. Sla het object met de data op in een variabele `const nameOfData = response.data`
10. Nu kun je elke object binnen je endpoint aanroepen door de naam van de variabele te gebruiken. Let op! Een endpoint kan een array of object zijn en/of bevatten. Je zult dus middels de juiste syntax moeten aanroepen op onze variabele nameOfDataObject (bijv. `nameOfData.obj[0].info`)
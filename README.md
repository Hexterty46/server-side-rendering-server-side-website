# Server-Side Website

Ontwerp en ontwikkel een server-side website voor een opdrachtgever

De instructie vind je in: [INSTRUCTIONS.md](https://github.com/fdnd-task/server-side-rendering-server-side-website/blob/main/docs/INSTRUCTIONS.md)


## Inhoudsopgave

  * [Beschrijving](#beschrijving)
  * [Gebruik](#gebruik)
  * [Kenmerken](#kenmerken)
  * [Installatie](#installatie)
  * [Bronnen](#bronnen)
  * [Licentie](#licentie)

## Beschrijving
<!-- In de Beschrijving staat kort beschreven wat voor project het is en wat je hebt gemaakt -->
<!-- Voeg een mooie poster visual toe 📸 -->
<!-- Voeg een link toe naar Github Pages 🌐-->
Check [hier](https://server-side-rendering-server-side-website-d2t6.onrender.com/) de website.

Tijdens deze sprint heb ik gefocust op het halen van data uit de Directus, en deze te kunnen renderen op de browser. Ik hbe in deze sprint data van de nieuwsartikelen opgehaald van de Algemeen pagina, een zoekfunctie gemaakt om artikelen makkelijker, en sneller te kunnen vinden, en tot slotte ook een sorteren functie gemaakt. _**Mobile First**_ & _**Content First**_ principe.

De website bestaat op dit moment uit de Home pagina op de mobile view

De Homepagina geeft een overzicht van belangrijke onderdelen van BuurtCampus. Ik heb kleuren uit de styleguide gebruikt maar anders toegepast zodat de pagina moderner er uit ziet.

<img width="436" height="827" alt="image" src="https://github.com/user-attachments/assets/8450d774-afee-4fec-a939-702c30909be5" />
<img width="365" height="717" alt="image" src="https://github.com/user-attachments/assets/53c70249-3875-443d-97e5-1a073118d943" />

## Gebruik
<!--Bij Gebruik staat hoe je project er uit ziet, hoe het werkt en wat je er mee kan. -->
Het is de bedoeling dat ik op de homepage alle artikelen die in de `algemeen` district zitten te zien krijg. De `oost`, `zuidoost`, `nieuw-west` hebben allemaal een eigen huisstijl behalve de `algemeen` pagina. Daarom wil ik deze zo neutraal mogelijk houden. Een nieuwsartikel bestaat uit een `cover` voor visuele aantrekking, een `title` voor belangerijk keywoards over het artikel, een `intro` om een kleine beschrijving te geven over de nieuwsartikel, en tot slotte is de `date`, om te kunnen zien wanneer een artikel is toegevoegd, en om ervoor te zorgen dat mensen hier op kunnen sorteren.

Ik heb ook een hamburger menu gemaakt met behulp van HTML, CSS en Javascript. De hamburger menu kan geopend worden, door op het MENU button te klikken. Vanuit het hamburger menu kan er genavigeert worden naar andere pagina's, inclusief de andere districten. Naaast de home pagina heb ik ook de `Nieuw-West` pagina gemakt om de filter parameter beter te begrijpen, en om een voorbeeld te geven hoe ik zou kunnen navigeren naar andere Districts.

<img width="382" height="813" alt="image" src="https://github.com/user-attachments/assets/caf953b3-3829-40d3-9ca9-a1b3a59e189f" />


## Kenmerken
<!-- Bij Kenmerken staat welke technieken zijn gebruikt en hoe. Wat is de HTML structuur? Wat zijn de belangrijkste dingen in CSS? Wat is er met Javascript gedaan en hoe? Misschien heb je een framwork of library gebruikt? -->
Er word gebruik gemaakt van een styleguide binnen de website. Om het in CSS makkelijker te maken welke kleuren ik moet gebruiken, op een plek waar dat moet.
https://github.com/Hexterty46/server-side-rendering-server-side-website/blob/32c9b9862ad6bffd54be2b1538efb4c2ac483536/public/styleguide.css#L1-L21

### Loops
In de code word er een Liquid loop gebruikt om de artiekels op te halen voor de homepagina.
Dit word gedaan door het gebruiken van `if/else` statements binnen Liquid. Ook gebruik ik de `if/else` statement voor als er geen afbeelding is bij de nieuwsartikel, dat ik dan een fallback afbeelding krijg. Hetzelfde geld ook vij de `date`. Als er geen `date` is aangegeven binnen de artikel, komt er een `Datum onbekend` te staan.
https://github.com/Hexterty46/server-side-rendering-server-side-website/blob/31bfca2082496349aed4883be5a53470d48a2c6b/views/index.liquid#L20-L45

### Hamburger menu
De hamburger menu is gemaakt volgens het [JavaScript 3 stappenplan](https://css-tricks.com/videos/150-hey-designers-know-one-thing-javascript-recommend/).

https://github.com/Hexterty46/server-side-rendering-server-side-website/blob/18a1af142de5949dc1468432c61b2b0c37ad9466/views/index.liquid#L9-L29
https://github.com/Hexterty46/server-side-rendering-server-side-website/blob/18a1af142de5949dc1468432c61b2b0c37ad9466/public/style.css#L96-L153
https://github.com/Hexterty46/server-side-rendering-server-side-website/blob/18a1af142de5949dc1468432c61b2b0c37ad9466/public/script.js#L1-L13

Voor de hamburger menu interactie is een [user tests](https://github.com/Hexterty46/the-web-is-for-everyone-interactive-functionality/issues/7) uitgevoerd.

### Search
Binnen de Home pagina kan ik naar atiekelen zoeken, om het makkelijker te maken om naar artikelen te zoeken binnen districten
https://github.com/Hexterty46/server-side-rendering-server-side-website/blob/32c9b9862ad6bffd54be2b1538efb4c2ac483536/server.js#L40-L63
https://github.com/Hexterty46/server-side-rendering-server-side-website/blob/18a1af142de5949dc1468432c61b2b0c37ad9466/views/partials/head.liquid#L38-L43

### Partials

Voor de website gebruik ik partials, zo kan ik makkelijk mijn Header en Footer op andere pagina's ook gebruiken.
https://github.com/Hexterty46/server-side-rendering-server-side-website/blob/31bfca2082496349aed4883be5a53470d48a2c6b/views/index.liquid#L1
https://github.com/Hexterty46/server-side-rendering-server-side-website/blob/31bfca2082496349aed4883be5a53470d48a2c6b/views/index.liquid#L47

## GET method
Ik heb data kunnen ophalen uit de databse doormiddel van een `GET` method te gebruiken in mijn `server.js`. Om te bepalen welke data ik wil ophalen, geef ik een `params` mee binnen de `GET`.
https://github.com/Hexterty46/server-side-rendering-server-side-website/blob/18a1af142de5949dc1468432c61b2b0c37ad9466/server.js#L40-L63

## Installatie
<!-- Bij Instalatie staat hoe een andere developer aan jouw repo kan werken -->
Volg deze stappen om de development omgeving in te richten om aan deze repository te kunnen werken:

Stap 1) Installeer de [NodeJS ontwikkelomgeving](https://nodejs.org/en/download). Kies voor NodeJS 24.13.0 (LTS, long-term support), download het installatiebestand en doorloop het installatieproces.

Stap 2) Fork deze repository, clone deze op jouw computer en open het in VSCodium/ een code editor.

Stap 3) Open de Terminal in VSCodium of VSCode, Voer in de terminal het commando npm install uit door het in te typen en op enter te drukken.

Stap 4 ) Na de installatie is de map node_modules aangemaakt, en gevuld met allerlei packages. Start de website door in de terminal het comando npm start uit te voeren. Als het goed is, komt hier een melding te staan over het opstarten van de server: Application started on http://localhost:8000 — Open deze URL in je browser.

## Bronnen
- [Liquid - if/else](https://shopify.dev/docs/api/liquid/tags/conditional-else)
- [JavaScript - 3 stappenplan](https://css-tricks.com/videos/150-hey-designers-know-one-thing-javascript-recommend/)
- [De Volkskrant - inspiratie](https://www.volkskrant.nl/)
- [NodeJS download](https://nodejs.org/en/download)

## Licentie

This project is licensed under the terms of the [MIT license](./LICENSE).

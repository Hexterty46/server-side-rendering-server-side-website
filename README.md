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

De website bestaat op dit moment uit de Home pagina op de mobile view

De Homepagina geeft een overzicht van belangrijke onderdelen van BuurtCampus. Ik heb kleuren uit de styleguide gebruikt maar anders toegepast zodat de pagina moderner er uit ziet.

## Gebruik
<!--Bij Gebruik staat hoe je project er uit ziet, hoe het werkt en wat je er mee kan. -->

## Kenmerken
<!-- Bij Kenmerken staat welke technieken zijn gebruikt en hoe. Wat is de HTML structuur? Wat zijn de belangrijkste dingen in CSS? Wat is er met Javascript gedaan en hoe? Misschien heb je een framwork of library gebruikt? -->
Er word gebruik gemaakt van een styleguide binnen de website.
https://github.com/Hexterty46/server-side-rendering-server-side-website/blob/32c9b9862ad6bffd54be2b1538efb4c2ac483536/public/styleguide.css#L1-L21

### Loops
In de code word er een Liquid loop gebruikt om de artiekels op te halen voor de homepagina
https://github.com/Hexterty46/server-side-rendering-server-side-website/blob/31bfca2082496349aed4883be5a53470d48a2c6b/views/index.liquid#L20-L45

### Search
Binnen de Home pagina kan ik naar atiekelen zoeken
https://github.com/Hexterty46/server-side-rendering-server-side-website/blob/32c9b9862ad6bffd54be2b1538efb4c2ac483536/server.js#L40-L63

### Partials

Voor de website gebruik ik partials, zo kan ik makkelijk mijn Header en Footer op andere pagina's ook gebruiken.
https://github.com/Hexterty46/server-side-rendering-server-side-website/blob/31bfca2082496349aed4883be5a53470d48a2c6b/views/index.liquid#L1
https://github.com/Hexterty46/server-side-rendering-server-side-website/blob/31bfca2082496349aed4883be5a53470d48a2c6b/views/index.liquid#L47

## Installatie
<!-- Bij Instalatie staat hoe een andere developer aan jouw repo kan werken -->

## Bronnen

## Licentie

This project is licensed under the terms of the [MIT license](./LICENSE).

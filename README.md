# Wijnproeverij HC Eemvallei – bestel-app

Eén HTML-bestand (`index.html`) om op de proefavond snel bestellingen in te voeren.

**🌐 Open de app: https://hermanvandenberg.github.io/Wijnproeverij-HC-Eemvallei/**

- Per wijn flessen of dozen (6), extra wijnen uit het assortiment van Wijnhuis Alexander en geschenkkisten
- Automatisch totaal en een uniek referentienummer per bestelling (HCE-001, …)
- Tikkie: bedrag en omschrijving kopiëren, Tikkie-link plakken en via WhatsApp versturen
- Overzicht met zoeken, status betaald / opgehaald
- Picklijst per wijn (dozen + losse flessen) en printbare klaarzetbonnen
- Excel-export (.xlsx, of CSV zonder internet) en back-up / samenvoegen als JSON
- Betalen direct op de clubrekening: vul bij Instellingen het IBAN van de club in. Elke bestelling krijgt dan een betaal-QR-code (EPC/GiroCode-standaard) met bedrag en referentie, en het WhatsApp-bericht noemt IBAN, bedrag en referentie. Met **Stuur QR + tekst** gaat de QR-afbeelding met de tekst via WhatsApp naar de koper. Tikkie blijft beschikbaar als optie.
- Gasten bestellen zelf: bij Instellingen → *Gasten bestellen zelf* toon of print je een klant-QR. Gasten kiezen hun wijnen op hun eigen telefoon, krijgen een referentie (HCE-K-XXXX) en de betaalgegevens van de club, en sturen hun bestelling met één tik via WhatsApp naar de verzameltelefoon. Die tikt op de link in het bericht (of gebruikt *Klantbestelling plakken*) en de bestelling staat erin, met een prijscontrole tegen de eigen wijnlijst.
- In het overzicht staat per bestelling op welke telefoon hij is ingevoerd en of het betaalverzoek al verstuurd is (filter: *Betaalverzoek nog niet verstuurd*).
- Meerdere telefoons: elke telefoon krijgt een letter (HCE-A-001, HCE-B-001), bestellingen versturen via WhatsApp en samenvoegen op één telefoon (nieuwste wijziging wint, verwijderde bestellingen blijven weg)

## Laptops live koppelen (koppelcode)

1. Op de laptop die alles verzamelt: Instellingen → *Laptops live koppelen* → **Maak dit de centrale laptop**. Er verschijnt een koppelcode van 6 tekens.
2. Op elke andere laptop: kies bij *Meerdere telefoons* een eigen letter (B, C, D…), vul de koppelcode in en tik **Koppel**.
3. Elke bestelling en wijziging gaat direct naar de centrale. Prijzen, wijnlijst en IBAN van de centrale gaan automatisch naar alle laptops. Valt het internet even weg, dan blijven bestellingen in de wachtrij en worden ze vanzelf nagestuurd.

Dit werkt via een rechtstreekse verbinding tussen de browsers (WebRTC, PeerJS). Er is internet nodig; de bestellingen staan niet op een server. Werkt het netwerk niet mee, gebruik dan *Versturen* en *Samenvoegen* hieronder als terugvaloptie.

## Met meerdere telefoons

1. Open de app op elke telefoon en kies bovenaan bij *Nieuw* een andere letter (A, B, C…).
2. Zelfde wijnlijst nodig? Stuur vanaf de eerste telefoon via **Overzicht → Versturen** het bestand en kies op de andere telefoon **Samenvoegen**; beantwoord de vraag om de wijnlijst over te nemen met OK.
3. Tussendoor of aan het eind: elke telefoon **Versturen** via WhatsApp naar de verzamel-telefoon, die **Samenvoegen** doet. Je kunt vaker samenvoegen; dubbele bestellingen worden herkend.

Gegevens worden alleen in de browser van het apparaat bewaard (localStorage). Maak dus een back-up.

Openen: ga naar https://hermanvandenberg.github.io/Wijnproeverij-HC-Eemvallei/ (GitHub Pages), of download `index.html` en open het in de browser.

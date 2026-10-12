# Krimphoes configurator

Webtool van Gerbri BV voor krimphoezen. De klant voert de afmetingen van de pallet in (lengte, breedte, hoogte), plaatst een logo en ziet direct een 3D-weergave van de pallet met stenen en krimphoes. Met de knop "EPS-bestand maken" downloadt de klant een EPS-bestand dat naar de drukker kan.

De pagina is één statisch HTML-bestand zonder backend. three.js (r128) en de lettertypes Ubuntu en Roboto staan in deze repo (`vendor/` en `fonts/`), zodat er geen gegevens van bezoekers naar externe servers gaan.

## URL

Na publicatie via GitHub Pages staat de tool op:

https://juliang138.github.io/krimphoes-configurator/

## Lokaal testen

Start in de map van de repo een eenvoudige webserver:

```sh
python3 -m http.server
```

Open daarna http://localhost:8000 in de browser.

## Update uitrollen

1. Vervang `index.html` door de nieuwe versie (bestandsnaam `index.html` houden).
2. Commit en push naar `main`:

   ```sh
   git add index.html
   git commit -m "Update configurator"
   git push origin main
   ```

GitHub Pages publiceert de nieuwe versie binnen een paar minuten.

## Eigen domein koppelen (optioneel)

1. Ga in GitHub naar **Settings > Pages** en vul bij **Custom domain** het domein in, bijvoorbeeld `configurator.gerbri.nl`. Klik op **Save**.
2. Maak bij de domeinbeheerder een **CNAME-record** aan voor die subdomeinnaam met als waarde `juliang138.github.io`.
3. Wacht tot de DNS-wijziging actief is en zet daarna in **Settings > Pages** het vinkje **Enforce HTTPS** aan.

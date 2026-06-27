# Immo_Webscraping
Schreibt einen auf Pythons Selenium basierenden Bot, um Daten zu zum Verkauf stehenden Häusern von [ImmobilienScout24](https://www.immobilienscout24.de/) zu sammeln. Es sei darauf hingewiesen, dass der Code nur zur Veranschaulichung dient und nicht aktiv genutzt werden sollte, da der Webseiten-Betreiber Richtlinien gegen Webscraping haben könnte.

## Grundlage
Wir schreiben Code, um Pythons Paket `selenium` zusammen mit `selenium_stealth` und `undetected_chromedriver` zu nutzen, um einen Chrome-Browser manuell durch die Suchliste von ImmobilienScout24 zu navigieren, Seiten zu Immobilien nacheinander zu öffnen und die Verkaufsdaten in einem `pandas` dataframe zu speichern. Als Beispiel nutzen wir hier die Suchergebnisse der zum Verkauf stehenden Häuser im Kreis Paderborn in Nordrhein-Westfalen (sortiert von den neuesten Einträgen zu den ältesten), jedoch kann der Code theoretisch für andere Suchen genutzt werden.

## Hinweise vorweg
ImmobilienScout24 nutzt Anti-Bot-Software, um botgesteuerte Browser zu erkennen und Scraping-Versuche entweder zu verlangsamen oder auch mit CAPTCHAs zu unterbrechen. Schon beim ersten Öffnen der Seite könnte man mit einem CAPTCHA konfrontiert werden. Daher nutzen wir hier `selenium`. Dies ermöglicht uns, mit dem ferngesteuerten Browser manuell interagieren zu können, sollten wir auf Hindernisse wie CAPTCHAs treffen. Dem aktuellen Stand nach vom 27.06.2026 könnte man beim ersten Öffnen der Seite auf ein CAPTCHA treffen sowie jeweils nach dem Scrapen von ca. 450 Einträgen. Auch Tools wie `undetected_chromedriver` und `selenium_stealth` helfen derzeit nicht mehr weiter.


# Entwicklungsplan Murmelwerk

## Ausgangsstand
V13 der Offline-Web-App ist die technische Basis. Die 12-mm-Rasterlogik und eine erste 3D-Kamera sind vorhanden; mechanische Genauigkeit ist noch nicht ausreichend für garantierte Nachbaubarkeit.

## Prioritäten
1. **Mechanische Schnittstellen**: Jede Schiene sitzt ausschließlich oberhalb/unterhalb von Blöcken oder violetten Zwischenplättchen. Verbindungsmöglichkeiten bei übereinanderliegenden Schienen mit mittleren Öffnungen prüfen.
2. **Geometrie**: Relative Positionen aller Lochmittelpunkte der drei erfassten Kurven- und S-Schienen messen. Keine Schienen durch Holzkörper und keine räumlichen Kollisionen.
3. **Mehrstöckiger Generator**: Verzweigungen, Rückführungen und übereinanderliegende Strecken mit gültigem Weggraphen. Keine unverbundenen benutzten Ausgänge.
4. **Bauteile**: Naturholz, gelb, orange, grün, türkis, blau, rot mit Aufdruck und Zubehör. Unbekannte Teile bleiben im Katalog sichtbar und werden nicht ohne verifizierte Regeln eingesetzt.
5. **Stopfen und Keile**: Für grünen Horizontal-Durchgang Lochabdeckung verbrauchen. Bei jedem tatsächlich genutzten Weg von TOP zu SIDE einen Beschleunigerkeil einplanen. Roter Verteiler benötigt zwei gültige angeschlossene Ausgänge.
6. **Melodietreppe**: geneigte Sonderverbindung `SIDE_OUT → TOP_IN`, 12-mm-Endstücke; Neigung und Anschlussgeometrie sind noch zu messen.
7. **3D-Modelle**: Referenzmodelle anhand echter Bauteile präzisieren und nach erfolgreicher Validierung in den Generator integrieren.
8. **UI**: freie 360°-Kamera, Verschieben, stabiler Touch-Zoom und neuer Entwurf per Button statt festen Varianten. Inventar lokal persistent speichern.

## Validierung
- Alle erreichbaren Kugelpfade enden an einem kompatiblen Folgeelement.
- Angeschlossene Routen sind mit der gemeinsamen Drehung eines Blocks konsistent.
- Stützen, Schienen und Zusatzteile werden vollständig aus dem Inventar abgezogen.
- Nutzer-Toleranz 5–50 % für ungenutzte Teile; bei Nichterreichbarkeit explizit anzeigen.
- Referenzbauten aus den Hape-Anleitungen zur Regression verwenden, ohne die Pläne unberechtigt zu übernehmen.

## Daten
`data/bauteilbibliothek.json` und `data/schienen.json` enthalten den bisherigen Forschungsstand. Sie sind ausdrücklich nicht in allen technischen Eigenschaften verifiziert.

# Familien-Lernpilot – statisches Releasepaket

Dieses Paket ist eine direkt bereitstellbare, statische Browser-App. Es enthält keine vorbereiteten Beobachtungen, keine Namen von Kindern und keine Exportdateien.

## Technische Eigenschaften

- Relative Pfade: `index.html` lädt ausschliesslich `styles.css` und `app.js` aus demselben Ordner.
- Keine API-Aufrufe, keine Cloud-Datenbank, keine Anmeldung, kein Tracking und keine externe Schrift- oder Medienquelle.
- Der lokale Stand liegt erst nach Benutzung im Browser-`localStorage` unter `familien-lernpilot-static-v1`.
- PC und iPhone behalten getrennte lokale Stände. Export und Import sind eine bewusste Dateiübertragung; Import ersetzt den Stand auf dem Zielgerät und führt nichts zusammen.
- Das Wochenblatt bleibt über die PC-Browser-Druckfunktion verfügbar. Physische Drucker wurden nicht getestet.

## Lokale Vorschau

Für eine zuverlässige lokale Vorschau einen beliebigen temporären statischen Server verwenden und dessen lokale Adresse öffnen. Die Bedienung der später bereitgestellten Online-Ausgabe benötigt keinen eigenen Serverprozess.

Direktes Öffnen über `file:` ist nur eine optische Vorschau: Browser behandeln `localStorage` bei `file:` nicht einheitlich. Für echte Bedien- und Speichertests deshalb die veröffentlichte HTTPS-Adresse oder eine temporäre lokale HTTP-Vorschau verwenden.

## Vor einer Veröffentlichung prüfen

1. Ausschliesslich diesen Ordner hochladen, niemals lokale JSON-Exporte oder Inhalte aus vorherigen lokalen Arbeitsordnern.
2. Über die fertige HTTPS-Adresse auf PC und iPhone öffnen und prüfen, dass die leere Startansicht erscheint.
3. Einen rein fiktiven Eintrag testen, Export/Import kontrollieren und anschliessend wieder zurücksetzen.
4. Den PC-Druckdialog und den tatsächlichen Drucker separat prüfen.

Siehe `DEPLOYMENT-OPTIONEN.md` für die bewusst noch nicht ausgeführte Bereitstellung.

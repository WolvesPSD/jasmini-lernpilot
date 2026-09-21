# DEPLOYMENT-OPTIONEN – noch nicht ausgeführt

Stand: 21. September 2026  
Paket: `familien-lernpilot-static-v1`

## Feste Grenzen

Dieses Paket enthält nur statische App-Dateien. Es lädt keine Lernstände auf einen Server: Jede Eingabe bleibt im Browser des jeweiligen Geräts, bis eine erwachsene Person bewusst eine JSON-Datei exportiert und auf einem anderen Gerät importiert. Ein öffentlicher Link schützt weder lokale Browserdaten noch JSON-Exporte. Es dürfen daher keine Exportdateien oder echten Kinddaten hochgeladen werden.

Ein statischer Host kann trotzdem technische Zugriffsdaten wie IP-Adresse, Zeitpunkt und Browserdaten verarbeiten. Das ist von einer App-Datenbank zu unterscheiden, aber vor einer echten Familienfreigabe transparent zu entscheiden.

## OneDrive: Dateifreigabe, kein zugesichertes App-Hosting

OneDrive ist als Speicher- und Freigabedienst für Dateien oder Ordner zu bewerten. Microsoft beschreibt Freigabelinks als Berechtigung für ein Element; je nach Linktyp sind sie anonym, organisationsweit oder auf bestimmte Personen eingeschränkt. Das ist kein Zusagevertrag für die Auslieferung einer Browser-App mit passendem HTML-MIME-Typ, stabilen relativen Pfaden, Cache-Verhalten oder einer direkt öffnenden Startseite.

Darum OneDrive nicht als bevorzugtes App-Hosting festlegen. Es könnte später nur nach einem konkreten PC- und iPhone-Test als Dateizugang beurteilt werden. Kein Upload, keine Ordnerfreigabe und kein Link wurden erstellt.

Quellen: [Microsoft: shareable links](https://learn.microsoft.com/en-us/sharepoint/shareable-links-anyone-specific-people-organization), [Microsoft: Sharing items](https://learn.microsoft.com/en-us/onedrive/developer/rest-api/concepts/sharing?view=odsp-graph-online).

## Bevorzugte Option: GitHub Pages über GitHub Free

GitHub Pages veröffentlicht statische HTML-, CSS- und JavaScript-Dateien direkt aus einem Repository. Die offizielle GitHub-Dokumentation nennt GitHub Pages für öffentliche Repositories unter GitHub Free als verfügbar; die kleinste passende Einrichtung ist daher ein neues, ausschliesslich für dieses Release bestimmtes öffentliches Repository mit der Veröffentlichung aus dem Hauptbranch und dessen Stammordner. Die Datei `.nojekyll` stellt sicher, dass die statischen Dateien unverändert ausgeliefert werden.

Dieser Weg ist öffentlich: Der Code und die generischen Aufgaben sind mit der Repository-URL einsehbar. GitHub weist zudem darauf hin, dass GitHub Pages beim Besuch IP-Adressen zu Sicherheitszwecken protokolliert. Das Release enthält deshalb keine Namen, Exportdateien oder Lernstände.

Nicht verwenden: GitHub Actions mit zusätzlichem Build, Datenbanken, Analytics-SDKs oder andere Drittanbieter. Sie sind für dieses Paket nicht nötig und würden die klare lokale Datenhaltung verändern.

Quellen: [GitHub Pages: Was ist das?](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages), [GitHub Pages aus einem Branch veröffentlichen](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site), [GitHub Pages erstellen](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).

## Alternative: Cloudflare Pages, direkter statischer Upload

Cloudflare Pages bleibt eine später mögliche statische Alternative. Sie wurde nicht ausgewählt und nicht eingerichtet. Die bisherige Einschätzung dazu ist absichtlich keine Veröffentlichungsempfehlung mehr.

## Kleinste spätere Veröffentlichungserlaubnis

Eine ausdrückliche Freigabe wäre nötig für genau diesen Vorgang:

> Eine vorhandene GitHub-Anmeldung verwenden, ein neues öffentliches Repository nur für den Ordner `familien-lernpilot-static-v1` erstellen, dessen bereinigte Dateien hochladen, GitHub Pages aus dem Hauptbranch aktivieren und die erzeugte öffentliche `github.io`-Adresse an die Familie weitergeben.

Diese Freigabe umfasst weder das Hochladen von JSON-Exporten noch echte Kinddaten, keine Datenbank, keine Anmeldung in der App, keine Synchronisierung und keine zusätzlichen Drittanbieter. Erst nach der Freigabe den Upload und einen PC-/iPhone-HTTPS-Test durchführen.

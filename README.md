# felixkohle02.github.io

GitHub-Pages-Benutzer-Site (Domain-Wurzel `https://felixkohle02.github.io/`). Die Rechtstexte bleiben
im Projekt-Repo `legal` (`/legal/…`); diese Site trägt nur, was an der Wurzel liegen muss.

- `index.html` – kleine Startseite (Leita im Store, Rechtliche Hinweise).
- `leita/c/index.html` – Landeseite der Leita-Herausforderungslinks (`/leita/c/?k=<CODE>`): bietet
  „In Leita öffnen“ (`leita://c/?k=…`, auf Chrome als `intent://` mit Store-Rückfall) und den
  Play-Store-Link; statisch, keine Skripte von Dritten.
- `.well-known/assetlinks.json` – Android-App-Link-Verifizierung für `com.beavergoose.leita`.
  Enthalten: Fingerabdruck des **Upload-Zertifikats** (lokal signierte QA-Builds). **Offen:** der
  Fingerabdruck des **App-Signing-Zertifikats** aus der Play Console (Testen und veröffentlichen →
  App-Integrität → App-Signatur → SHA-256) – erst damit öffnen Store-Installationen https-Links direkt.
- `.nojekyll` – damit GitHub Pages den Punkt-Ordner `.well-known` ausliefert.

Veröffentlichen (nur auf Felix' Wort): auf GitHub ein öffentliches Repo `felixkohle02.github.io`
anlegen, `git remote add origin https://github.com/felixkohle02/felixkohle02.github.io.git`,
`git push -u origin main`. Prüfen: `https://felixkohle02.github.io/.well-known/assetlinks.json`
muss als JSON erreichbar sein (HTTP 200, kein Redirect).

Format des Codes und Datenfluss: `produkte/wortraum/docs/CHALLENGE_LINKS.md` im Business-Workspace.

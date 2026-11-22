# An-Naba Bilderbuch

Surat an-Naba, Ayat 1–30, als Bilderbuch in sechs Blöcken:

- **Ayat**: Wort für Wort mit Harakat, farbkodiert (rot Verb, blau Nomen, grün Partikel, schwarz Name und Versnummer), Deutsch darunter
- **Geschichte**: ein Satz pro Seite mit Bild; alle Wörter der Ayat kommen darin vor (gelb hinterlegt)
- **Spiele**: Bedeutung, Paare finden, Welche Farbe?, Lücke in der Aya

Fortschritt, Spielergebnisse und schwierige Wörter werden pro Nutzer in Firestore unter `users/{uid}/entries` gespeichert. Nur der angemeldete Nutzer kann seine Daten lesen (siehe `firestore.rules`). Ohne Anmeldung wird auf dem Gerät gespeichert.

## Einrichtung
1. Firebase-Konsole → Projekt erstellen → **Web-App** hinzufügen → Config in `firebase-config.js` einfügen.
2. **Authentication** → Sign-in method → **Google** aktivieren.
3. Authentication → Settings → **Authorized domains** → `athleticconsumer-dotcom.github.io` hinzufügen.
4. **Firestore Database** → im **Production mode** erstellen → Tab Rules → Inhalt von `firestore.rules` einfügen → Publish.
5. GitHub-Repo → Settings → **Pages** → Deploy from branch `main`, Ordner `/ (root)`.
6. `https://athleticconsumer-dotcom.github.io/<repo-name>/` öffnen, mit Google anmelden, fertig.

## App
Installierbar (PWA): Android Chrome → Menü → App installieren. iPhone: Safari → Teilen → Zum Home-Bildschirm.

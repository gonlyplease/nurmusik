# Nur Musik – Einrichtung (ca. 15 Minuten, einmalig)

Du brauchst: Spotify Premium, ein kostenloses GitHub-Konto und dein iPhone. Die Schritte gehen auch komplett am iPhone in Safari, am Computer ist es aber bequemer.

## 1. Seite online stellen (GitHub Pages, kostenlos)
1. Auf github.com anmelden und rechts oben auf **+ → New repository** gehen.
2. Name z. B. `nurmusik`, **Public** auswählen und **Create repository** tippen.
3. Auf **uploading an existing file** tippen und diese 4 Dateien hochladen:
   `index.html`, `icon-180.png`, `icon-512.png`, `manifest.webmanifest`.
   Danach **Commit changes** tippen.
4. Im Repository **Settings → Pages** öffnen. Bei *Branch* `main` und `/ (root)` wählen und **Save** tippen.
5. Nach 1–2 Minuten ist die Seite erreichbar unter:
   `https://DEIN-GITHUB-NAME.github.io/nurmusik/`

## 2. Spotify-App anlegen
1. developer.spotify.com/dashboard öffnen und mit deinem Spotify-Konto anmelden.
2. **Create app** wählen:
   - Name/Beschreibung: beliebig (z. B. „Nur Musik“)
   - **Redirect URI**: genau die Adresse aus Schritt 1.5, mit Schrägstrich am Ende.
     Die Seite zeigt sie dir beim ersten Öffnen auch noch einmal an.
   - Bei „Which API/SDKs“ **Web API** anhaken und speichern.
3. Die **Client ID** kopieren. Sie besteht aus 32 Zeichen.

## 3. Am iPhone einrichten
1. Die Adresse in **Safari** öffnen, die Client ID einfügen und **Weiter zur Anmeldung** tippen.
2. Bei Spotify anmelden und den Zugriff erlauben.
3. Auf **Teilen → Zum Home-Bildschirm** tippen. „Als Web-App öffnen“ eingeschaltet lassen.
4. Ab jetzt nur noch über das neue Symbol „Nur Musik“ starten.
   Falls du im Home-Bildschirm-Symbol noch einmal angemeldet werden musst, ist das normal: Die Web-App hat einen eigenen Speicher.

## Gut zu wissen
- **Die Musik spielt die Spotify-App ab.** Nur Musik ist die Fernbedienung.
  Steht da „Kein Wiedergabegerät“, öffne Spotify kurz (Link in der Meldung oder im ⋯-Menü), geh zurück und tippe noch einmal.
  Läuft die Musik einmal, steuerst du auch über den Sperrbildschirm.
- **Fremde Playlists** (z. B. von Spotify erstellte) kannst du abspielen. Die Songliste zeigt Spotify seit 2026 aber nur für eigene Playlists an.
- **Geräte wechseln** (z. B. auf Lautsprecher oder PC): Tippe auf den Mini-Player und dann unten auf den Gerätenamen.
- Im ⋯-Menü findest du: Abmelden, Client ID ändern.

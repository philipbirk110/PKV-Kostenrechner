# PKV-Kostenrechner

Arztrechnungen erfassen, PKV-Erstattung und Eigenanteil gegenüberstellen und pro Jahr ausrechnen, ob sich Einreichen oder Selbstzahlen lohnt.

## Hochladen auf GitHub Pages

1. Auf github.com ein neues Repository anlegen, z. B. `pkv-kostenrechner`. Sichtbarkeit: **Public** (für GitHub Pages im kostenlosen Konto nötig – es liegen keine persönlichen Daten im Repository).
2. **Add file → Upload files** und alle Dateien aus diesem Ordner hineinziehen:
   `index.html`, `manifest.webmanifest`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`, `README.md`
3. **Settings → Pages → Build and deployment → Source: Deploy from a branch**, Branch `main`, Ordner `/ (root)`, **Save**.
4. Nach ein bis zwei Minuten läuft der Rechner unter `https://DEIN-NAME.github.io/pkv-kostenrechner/`.

## Auf den iPhone-Home-Bildschirm

Adresse in **Safari** öffnen → Teilen-Symbol → **Zum Home-Bildschirm**. Der Rechner startet dann wie eine App mit eigenem Symbol.

## Datenschutz und Sicherheit

- Auf GitHub liegt nur das leere Programm. Rechnungen, Fotos und Beträge verlassen dein Gerät nie.
- Beim Öffnen ist alles leer. Zum Weitermachen **Sicherung laden**.
- Die Sicherungsdatei (`.json`) ist mit AES-256 verschlüsselt. Der Schlüssel liegt zweimal bei: mit deinem **Sicherungscode** und mit deinem **Masterkey** verschlossen (PBKDF2, 250.000 Runden).
- Zwischendurch wird verschlüsselt auf dem Gerät zwischengespeichert. Beim nächsten Öffnen fragt der Rechner »Wiederherstellen« oder »Verwerfen«.
- Belegfotos und PDFs liegen verschlüsselt im Gerätespeicher und vollständig in der Sicherungsdatei.
- Sicherungscode und Masterkey lassen sich unter **Schlüssel** ändern.
- Ohne Sicherungsdatei und ohne Code bzw. Masterkey kommt niemand an die Daten – auch du nicht. Leg die Sicherung zusätzlich in iCloud Drive ab.

## Excel

- **Excel exportieren**: ein Blatt pro Jahr plus Blatt »Sicherung« für den 1:1-Import (ohne Fotos, unverschlüsselt).
- **Excel importieren**: liest einen Export dieses Rechners oder die Vorlage `PKV-Kostenrechner.xlsx` (Blätter Tarif, Rechnungen, Posten).

## Hinweis

Das automatische Auslesen von Fotos und PDFs funktioniert nur in der Claude-App. In dieser Version hängst du Belege an und trägst die Werte selbst ein. Alles andere – Sicherung, Jahres-PDF, Excel – funktioniert gleich.

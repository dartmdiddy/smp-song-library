# SMP Song Library

Responsive Website zum Sammeln von Songs aus Minecraft Scripted SMP Videos und zum Nachverfolgen ihrer Lizenzinformationen.

## GitHub Pages aktivieren
1. Öffne **Settings → Pages** in diesem Repository.
2. Wähle **GitHub Actions** als Build and deployment source.
3. Der Workflow in `.github/workflows/pages.yml` veröffentlicht die Seite bei einem Push auf `main` oder `master`.
4. Wenn GitHub Pages bereit ist, findest du die URL unter **Settings → Pages**.

## Songs hinzufügen
Füge in `songs.json` ein neues Objekt zum Array `songs` hinzu. Felder:
- `title`, `artist`: Songtitel und Künstler
- `status`: `unverified`, `copyright`, `verified` oder `free`
- `rights`, `license`, `notes`: Lizenznotizen
- `source`: Quelle oder Video
- `rightsUrl`: Rechte-/Kontaktquelle
- `downloadUrl`: nur einen legalen, verifizierten Download eintragen; sonst leer lassen
- `added`: Datum als YYYY-MM-DD

**Wichtig:** Nicht automatisch als copyrightfrei markieren. Ein Song auf YouTube ist nicht automatisch für eigene Videos freigegeben. Prüfe Lizenzbedingungen, Attribution und kommerzielle Nutzung, bevor du ihn als `free` kennzeichnest.

## Neue Songvorschläge
Der Button „Song vorschlagen“ öffnet ein GitHub Issue mit Feldern für einen Song-Link. Das ist ein Vorschlag zur Prüfung, keine automatische Bestätigung der Lizenz.

## Automatisierung
Die aktuelle Version veröffentlicht die Website automatisch nach Code-Änderungen. Sie erkennt noch nicht automatisch Musik in neuen Videos. Dafür wäre eine festgelegte Liste von YouTube-Kanälen/Playlists plus eine zusätzliche Erkennungs- und Prüf-Pipeline nötig; Video-Metadaten allein belegen nicht, welcher Song verwendet wird.

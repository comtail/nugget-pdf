# Start-Werbung (House Ad) für Nugget PDF Reader

Die App lädt bei jedem Start im Hintergrund `promo.json` von dieser Adresse:

    https://comtail.github.io/nugget-pdf/promo/promo.json

Was du dort einträgst, erscheint **ab dem nächsten App-Start** – ohne App-Update.

| Feld               | Bedeutung                                                         |
|--------------------|-------------------------------------------------------------------|
| `enabled`          | `true` = Werbung zeigen, `false` = keine Werbung                  |
| `imageUrl`         | Bild (PNG/JPG/WebP, max. 5 MB, **https**). Ideal: 1080 × 1920 px  |
| `clickUrl`         | Wohin ein Tippen auf das Bild führt (optional)                    |
| `durationSeconds`  | Anzeigedauer, 1–10 Sekunden                                       |
| `skipAfterSeconds` | Ab wann „Überspringen“ möglich ist (0 = sofort)                   |
| `backgroundColor`  | Farbe hinter dem Bild, z. B. `#17120A`                            |
| `validFrom` / `validUntil` | Optionaler Zeitraum, Format `JJJJ-MM-TT`                  |

Tipps:
- Neues Bild immer unter **neuem Dateinamen** hochladen (z. B. `ad-2026-12.png`) und `imageUrl` anpassen –
  so lädt jede App das neue Bild sicher nach.
- Datei löschen oder `enabled: false` → die Werbung verschwindet beim übernächsten Start.
- Die App zeigt das Bild immer mit dem Hinweis „Anzeige“.

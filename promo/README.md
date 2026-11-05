# Start-Werbung von Nugget PDF Reader ändern

Die App zeigt bei jedem Start 5 Sekunden lang das Bild `werbung.jpg`.
Wer darauf tippt, landet auf dem Link aus `promo.json`.

## Bild austauschen (im Browser)
1. Öffne https://github.com/comtail/nugget-pdf/tree/main/promo
2. Oben rechts **Add file → Upload files**
3. Dein neues Bild hineinziehen. **Es muss exakt `werbung.jpg` heißen** (JPG, Hochformat, ideal 1080 × 1920 px, max. 5 MB).
4. Unten **Commit changes** klicken. Fertig.

## Link ändern
1. Öffne https://github.com/comtail/nugget-pdf/blob/main/promo/promo.json
2. Auf den **Stift** (Edit) klicken
3. Hinter `"clickUrl":` deinen Link eintragen, z. B. `"https://deine-seite.de"` (mit Anführungszeichen, muss mit https:// beginnen)
4. **Commit changes** klicken.

## Wann sieht man die Änderung?
GitHub braucht 1–2 Minuten zum Veröffentlichen, danach bis zu 10 Minuten Zwischenspeicher.
Danach zeigt die App beim nächsten Start das neue Bild und den neuen Link.
Bei sehr langsamem Internet kommt das neue Bild erst einen Start später.

## Weitere Einstellungen in promo.json
| Feld               | Bedeutung                                              |
|--------------------|--------------------------------------------------------|
| `enabled`          | `true` = Werbung zeigen, `false` = keine Werbung        |
| `durationSeconds`  | Anzeigedauer in Sekunden (1–10), Standard 5             |
| `skipAfterSeconds` | Ab wann „Überspringen“ möglich ist (0 = sofort, 5 = nie vor Ende) |
| `backgroundColor`  | Farbe hinter dem Bild, falls es den Bildschirm nicht füllt |
| `validFrom` / `validUntil` | Optionaler Zeitraum, z. B. `"2026-12-01"`      |

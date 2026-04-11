🇬🇧 [English](#personal-puzzles) · 🇩🇪 [Deutsch](#personal-puzzles-deutsch)

---

# Personal Puzzles

**A customizable chess tactics trainer as a standalone HTML application**

Developed by Guido Gößling from [Bielefelder SK von 1883](https://www.bielefeldersk.de/) in collaboration with Claude AI.

**[Play now](https://guidogoessling.github.io/personal-puzzles/)**


## What is Personal Puzzles?

Personal Puzzles is a free chess tactics trainer that runs entirely in the browser — no installation, no login, no ads. The app is a single HTML file with 50,000 embedded puzzles from the Lichess database.

The name reflects the core idea: **everything is customizable.** Train exactly the way that works for you.


## Key Features

- **Fully customizable** — time limit, start rating, mistakes allowed, rating increase per puzzle, time increment, piece count, color preference and more

- **50,000 of the best Lichess puzzles** — selected by quality: popularity, play count, and even distribution across all difficulty levels

- **Powerful theme filter** — 74 tactical motifs in 8 categories, combinable with AND/OR logic; custom motif combinations possible (e.g. only rook+bishop mate, only king attack with discovered check)

- **Offline-capable** — all 50,000 puzzles fully embedded, no server required

- **Single file** — one HTML file, easy to embed on your club website

- **Sound engine** — piece sounds vary by piece weight and move distance (pawn: light and high-pitched → queen: heavy and deep; short moves quiet, long moves louder)

- **Stockfish analysis** — directly in review mode, no external API needed

- **Daily puzzle** — 366 curated puzzles, deterministic by date

- **Bilingual** — full DE/EN interface, auto-detected from browser language


## Settings

| Setting | Options |
| - | - |
| Time limit | 1 / 3 / 5 / 10 min / Unlimited / Custom (1–999 min) |
| Start rating | Very Easy (600) to Insane (3000) / Custom (0–3200) |
| Mistakes | 1 / 3 / 5 / Unlimited / Custom (1–99) |
| Increase | None / Slow (+10) to Very Fast (+50) / Custom |
| Time increment | 0 / 1 / 2 / 3 / 5 s per correct move / Custom |
| On mistake | Try again / Next puzzle |
| Color preference | Mixed / White / Black / Random |
| Theme filter | 74 motifs in 8 categories, AND/OR logic, custom combinations |
| Piece count | Dual range slider (3–32 pieces on board) |
| Sound | Moves / Tones / All / Off |
| Hints | Motifs / Piece / All / None |
| Show rating | On / Off |


## Theme Filter

- **74 tactical motifs** in 8 categories (mating patterns, tactics, endgame, opening, etc.)
- **AND logic** — only puzzles containing *all* selected motifs (e.g. fork + pin)
- **OR logic** — puzzles containing *at least one* selected motif
- **Custom combinations** — freely combine any motifs (e.g. only rook+bishop mate, only king attack with discovered check)
- **Step method** — predefined motif sets per level (1–5) for systematic training with cumulative progression


## Move Input

- **Click-click** — select piece, click destination
- **Drag & drop** — desktop and touch (mobile)
- **Keyboard input** — UCI (`e2e4`), SAN English (`Nf3`), SAN German (`Sf3`), long form (`Knight f3`), castling (`O-O`)


## Review Mode

- **Retry** — restore the starting position
- **Solution** — move sequence with navigation (⏮ ◀ ▶ ⏭)
- **Analysis** — free movement with linear FEN history
- **Stockfish** — depth-24 analysis, 3 variants, eval bar


## Sound Engine (Web Audio API)

- Piece sounds vary by piece weight and move distance
- Pawn: light and high-pitched → queen: heavy and deep
- Short moves quiet, long moves louder; knight has a distinctive jump character
- Capture: additional "falling" sound of the captured piece
- Solved: ascending triad; Wrong: low buzz tone


## More Features

- Highscores per settings combination
- Performance rating (Elo-based with time bonus/penalty)
- Daily puzzle (366 curated puzzles, deterministic by date)
- Board flips based on player color
- Last move highlighted green, selected piece blue, possible moves as dots
- All settings persistent (localStorage)
- Reset button


## Technical Stack

| Component | Technology |
| - | - |
| Language | Vanilla JavaScript (no framework) |
| Chess logic | chess.js (BSD-2-Clause) |
| Sound | Web Audio API + CC0 samples |
| Chess pieces | SVG (Wikimedia Commons style) |
| Chess analysis | Stockfish.js WASM (Blob Worker) |
| Architecture | Single-file HTML |
| Storage | localStorage |


## Puzzle Data

- **50,000 puzzles** from the [Lichess puzzle database](https://database.lichess.org/#puzzles) — approximately 1% of the full Lichess database, selected by quality
- **License:** CC0 (Public Domain)
- **Selection criteria:** Popularity ≥ 50 (top third), high play count (NbPlays), rating 400–3200, even distribution across all difficulty levels, rarity bonus for uncommon tactical motifs
- **Format:** `["ID", "FEN", "Moves", Rating, "Themes"]`


## Usage

### As a player

Just open the page — no download, no installation: 👉 **[bielefeldersk.de/personalpuzzles](https://www.bielefeldersk.de/personalpuzzles)**

### Embed on your club website

Download `PP_36.html` and place it directly on your own server or insert it into an HTML embed window (e.g. Wix, Jimdo, WordPress).

### Run locally

```
Download PP_36.html → open in browser → done
```

No web server, no build step, no dependencies.


## License

| Component | License |
| - | - |
| Code | MIT License — Copyright © 2025–2026 Guido Gößling / Bielefelder SK von 1883 e.V. |
| Puzzle data | CC0 (Lichess) |
| Sound samples | CC0 (Freesound.org) |
| chess.js | BSD-2-Clause |
| Chess piece SVGs | CC BY-SA (Wikimedia Commons) |


## About the Author

Personal Puzzles was developed by **Guido Gößling** from **[Bielefelder SK von 1883 e.V.](https://www.bielefeldersk.de/)**

Questions, ideas, suggestions: [guido.goessling@web.de](mailto:guido.goessling@web.de)


## Version History

| Version | Date | Highlights |
| - | - | - |
| PP_36 | 08.04.2026 | Bilingual interface (DE/EN), auto language detection, language toggle |
| PP_35 | 02.04.2026 | Settings persistence, piece count filter, reset button |
| PP_34 | 03.03.2026 | Settings reorganization, time increment, color preference, extended settings |
| PP_33 | 28.02.2026 | State object refactoring (reviewState, analysisState, sfState) |
| PP_32 | 20.02.2026 | Stockfish integration, analysis mode, eval bar |
| PP_31 | 18.02.2026 | Deselect, hint move count, grid preview, mating patterns |
| PP_30 | — | Daily puzzle system + widget |
| PP_24 | — | 50,000 puzzles, theme filter |

---

# Personal Puzzles (Deutsch)

**Personalisierter Schachtaktik-Trainer als standalone HTML-Anwendung**

Entwickelt von Guido Gößling vom [Bielefelder SK von 1883](https://www.bielefeldersk.de/) in Zusammenarbeit mit Claude AI.

**[Jetzt spielen](https://www.bielefeldersk.de/personalpuzzles)**


## Was ist Personal Puzzles?

Personal Puzzles ist ein kostenloser Schachtaktik-Trainer, der vollständig im Browser läuft — ohne Installation, ohne Login, ohne Werbung. Die Anwendung besteht aus einer einzigen HTML-Datei mit 50.000 eingebetteten Taktikaufgaben aus der Lichess-Datenbank.

Der Name steht für das Kernprinzip: **Alles ist personalisierbar.** Trainiere genau so, wie es für dich passt.


## Alleinstellungsmerkmale

- **Vollständig personalisierbar** — Zeitlimit, Startrating, Fehlversuche, Steigerung, Bonuszeit, Figurenanzahl, Farbauswahl und mehr

- **50.000 der besten Lichess-Puzzles** — ausgewählt nach Qualität: Popularität, Spielanzahl und gleichmäßiger Verteilung über alle Schwierigkeitsstufen

- **Mächtiger Themen-Filter** — 74 taktische Motive in 8 Kategorien, kombinierbar mit UND- und ODER-Logik; eigene Motivkombinationen möglich (z.B. nur Turm-Läufer-Matt, nur Königsangriff mit Abzugsschach)

- **Offline-fähig** — 50.000 Puzzles vollständig eingebettet, kein Server nötig

- **Single-File** — eine einzige HTML-Datei, einfach auf der eigenen Vereinsseite einzubinden

- **Sound-Engine** — Figurenklänge variieren nach Figurengewicht und Zugdistanz (Bauer: leicht und hoch → Dame: schwer und tief; kurze Züge leise, lange Züge lauter)

- **Stockfish-Analyse** — direkt im Review-Modus, ohne externe API

- **Tägliches Puzzle** — 366 kuratierte Puzzles, deterministisch per Datum

- **Zweisprachig** — vollständige DE/EN-Oberfläche, automatisch per Browsersprache erkannt


## Einstellungen

| Einstellung | Optionen |
| - | - |
| Zeitlimit | 1 / 3 / 5 / 10 min / Unbegrenzt / Personal (1–999 min) |
| Startrating | Sehr Leicht (600) bis Verrückt (3000) / Personal (0–3200) |
| Fehlversuche | 1 / 3 / 5 / Unbegrenzt / Personal (1–99) |
| Steigerung | Keine / Langsam (+10) bis Sehr Schnell (+50) / Personal |
| Bonuszeit | 0 / 1 / 2 / 3 / 5 s pro richtigem Zug / Personal |
| Bei Fehler | Nochmal probieren / Nächste Aufgabe |
| Farbauswahl | Gemischt / Weiß / Schwarz / Zufällig |
| Themen-Filter | 74 Motive in 8 Kategorien, UND/ODER-Logik, eigene Kombinationen |
| Figurenanzahl | Dual Range Slider (3–32 Figuren auf dem Brett) |
| Ton | Züge / Töne / Alles / Aus |
| Tipps | Motive / Figur / Alle / Keine |
| Rating anzeigen | Ein / Aus |


## Themen-Filter

- **74 taktische Motive** in 8 Kategorien (Matt-Motive, Taktiken, Endspiel, Eröffnung, u.a.)
- **UND-Logik** — nur Puzzles die *alle* gewählten Motive enthalten (z.B. Gabel + Fesselung)
- **ODER-Logik** — Puzzles die *mindestens eines* der gewählten Motive enthalten
- **Eigene Kombinationen** — beliebige Motivkombinationen frei zusammenstellbar (z.B. nur Turm-Läufer-Matt, nur Königsangriff mit Abzugsschach)
- **Stufen-Methode** — vordefinierte Motivsets pro Stufe (1–5) für systematisches Training mit kumulativem Aufbau


## Zugeingabe

- **Klick-Klick** — Figur wählen, Zielfeld klicken
- **Drag & Drop** — Desktop und Touch (Mobile)
- **Tastatureingabe** — UCI (`e2e4`), SAN englisch (`Nf3`), SAN deutsch (`Sf3`), Langform (`Springer f3`), Rochade (`O-O`)


## Review-Modus

- **Nochmal** — Ausgangsstellung wiederherstellen
- **Lösung** — Zugfolge mit Navigation (⏮ ◀ ▶ ⏭)
- **Analyse** — freies Ziehen mit linearer FEN-History
- **Stockfish** — Tiefe-24-Analyse, 3 Varianten, Eval-Bar


## Sound-Engine (Web Audio API)

- Figurenklänge variieren nach Figurengewicht und Zugdistanz
- Bauer: leicht und hoch — Dame: schwer und tief
- Kurze Züge leise, lange Züge lauter; Springer mit Sprungcharakter
- Schlagen: zusätzlicher „Umfall"-Sound der geschlagenen Figur
- Gelöst: aufsteigender Dreiklang; Falsch: tiefer Buzz-Ton


## Weiteres

- Highscores pro Einstellungs-Kombination
- Performance-Rating (Elo-basiert mit Zeit-Bonus/Malus)
- Tägliches Puzzle (366 kuratierte Aufgaben, deterministisch per Datum)
- Brett dreht sich je nach Spielerfarbe
- Letzter Zug grün markiert, ausgewählte Figur blau, mögliche Züge als Punkte
- Alle Einstellungen persistent (localStorage)
- Zurücksetzen-Button


## Technischer Stack

| Komponente | Technologie |
| - | - |
| Sprache | Vanilla JavaScript (kein Framework) |
| Schachlogik | chess.js (BSD-2-Clause) |
| Sound | Web Audio API + CC0-Samples |
| Schachfiguren | SVG (Wikimedia Commons Style) |
| Schachanalyse | Stockfish.js WASM (Blob-Worker) |
| Architektur | Single-File HTML |
| Datenspeicherung | localStorage |


## Puzzle-Daten

- **50.000 Puzzles** aus der [Lichess-Puzzle-Datenbank](https://database.lichess.org/#puzzles) — ca. 1% der gesamten Lichess-Datenbank, ausgewählt nach Qualität
- **Lizenz:** CC0 (Public Domain)
- **Auswahlkriterien:** Popularity ≥ 50 (oberes Drittel), hohe Spielanzahl (NbPlays), Rating 400–3200, gleichmäßige Verteilung über alle Schwierigkeitsstufen, Rarity-Bonus für seltene taktische Motive
- **Format:** `["ID", "FEN", "Moves", Rating, "Themes"]`


## Verwendung

### Als Spieler

Einfach die Seite öffnen — kein Download, keine Installation: 👉 **[bielefeldersk.de/personalpuzzles](https://www.bielefeldersk.de/personalpuzzles)**

### Auf der eigenen Vereinsseite einbinden

Die Datei `PP_36.html` herunterladen und direkt auf dem eigenen Server ablegen oder in ein HTML-Embed-Fenster einfügen (z.B. Wix, Jimdo, WordPress).

### Lokal ausführen

```
PP_36.html herunterladen → im Browser öffnen → fertig
```

Kein Webserver, kein Build-Schritt, keine Abhängigkeiten.


## Lizenz

| Komponente | Lizenz |
| - | - |
| Code | MIT License — Copyright © 2025–2026 Guido Gößling / Bielefelder SK von 1883 e.V. |
| Puzzle-Daten | CC0 (Lichess) |
| Sound-Samples | CC0 (Freesound.org) |
| chess.js | BSD-2-Clause |
| Schachfiguren SVG | CC BY-SA (Wikimedia Commons) |


## Über den Autor

Personal Puzzles wurde entwickelt von **Guido Gößling** vom **[Bielefelder SK von 1883 e.V.](https://www.bielefeldersk.de/)**

Fragen, Ideen, Verbesserungsvorschläge: [guido.goessling@web.de](mailto:guido.goessling@web.de)


## Versionsverlauf

| Version | Datum | Highlights |
| - | - | - |
| PP_36 | 08.04.2026 | Zweisprachige Oberfläche (DE/EN), automatische Spracherkennung, Sprach-Toggle |
| PP_35 | 02.04.2026 | Settings-Persistenz, Figurenanzahl-Filter, Zurücksetzen-Button |
| PP_34 | 03.03.2026 | Settings-Reorganisation, Bonuszeit, Farbauswahl, Erweiterte Einstellungen |
| PP_33 | 28.02.2026 | State-Objekt-Refactoring (reviewState, analysisState, sfState) |
| PP_32 | 20.02.2026 | Stockfish-Integration, Analyse-Modus, Eval-Bar |
| PP_31 | 18.02.2026 | Deselect, Hint-Zuganzahl, Grid-Vorschau, Matt-Motive |
| PP_30 | — | Daily Puzzle System + Widget |
| PP_24 | — | 50.000 Puzzles, Themen-Filter |

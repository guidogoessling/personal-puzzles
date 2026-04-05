# Personal Puzzles

**Personalisierter Schachtaktik-Trainer als standalone HTML-Anwendung**

Entwickelt vom [Bielefelder SK von 1883](https://www.bielefeldersk.de/) in Zusammenarbeit mit Claude AI.

**[Jetzt spielen](https://www.bielefeldersk.de/personalpuzzles)**


## Was ist Personal Puzzles?

Personal Puzzles ist ein kostenloser Schachtaktik-Trainer, der vollständig im Browser läuft — ohne Installation, ohne Login, ohne Werbung. Die Anwendung besteht aus einer einzigen HTML-Datei mit 50.000 eingebetteten Taktikaufgaben aus der Lichess-Datenbank.

Der Name steht für das Kernprinzip: **Alles ist personalisierbar.** Schwierigkeit, Zeitlimit, Fehlerzahl, Bonuszeit, Figurenanzahl, Spielerfarbe — jeder trainiert so, wie es für ihn passt.


## Alleinstellungsmerkmale

- **Offline-fähig** — 50.000 Puzzles vollständig eingebettet, kein Server nötig

- **Single-File** — eine einzige HTML-Datei, einfach weiterzugeben und einzubinden

- **Vollständig personalisierbar** — alle relevanten Trainingsparameter einstellbar

- **Hochwertige Sound-Engine** — hybride Web Audio API mit echten Holzsamples und Synthese; Tonhöhe und Lautstärke variieren nach Figurengewicht

- **Stockfish-Analyse** — direkt im Review-Modus, ohne externe API

- **Mächtiger Themen-Filter** — 74 taktische Motive in 8 Kategorien, kombinierbar mit UND- und ODER-Logik; eigene Motivkombinationen möglich (z.B. nur Turm-Läufer-Matt)

- **Tägliches Puzzle** — 366 kuratierte Puzzles, deterministisch per Datum

- **Keine externen Abhängigkeiten** — außer chess.js (CDN)


## Features

### Einstellungen

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


### Themen-Filter

- **74 taktische Motive** in 8 Kategorien (Matt-Motive, Taktiken, Endspiel, Eröffnung, u.a.)

- **UND-Logik** — nur Puzzles die *alle* gewählten Motive enthalten (z.B. Gabel + Fesselung)

- **ODER-Logik** — Puzzles die *mindestens eines* der gewählten Motive enthalten

- **Eigene Kombinationen** — beliebige Motivkombinationen frei zusammenstellbar (z.B. nur Turm-Läufer-Matt, nur Königsangriff mit Abzugsschach)

- **Stufen-Methode** — vordefinierte Motivsets pro Stufe (1–5) für systematisches Training, mit kumulativem Aufbau

### Zugeingabe

- **Klick-Klick** — Figur wählen, Zielfeld klicken

- **Drag & Drop** — Desktop und Touch (Mobile)

- **Tastatureingabe** — UCI (`e2e4`), SAN deutsch (`Sf3`), SAN englisch (`Nf3`), Langform (`Springer f3`), Rochade (`O-O`)

### Review-Modus

- **Nochmal** — Ausgangsstellung wiederherstellen

- **Lösung** — Zugfolge mit Navigation (⏮ ◀ ▶ ⏭)

- **Analyse** — freies Ziehen mit linearer FEN-History

- **Stockfish** — Tiefe-24-Analyse, 3 Varianten, Eval-Bar

### Sound-Engine (Web Audio API)

- Abheben und Absetzen mit variabler Pause je nach Zugdistanz

- Tonhöhe und Lautstärke variieren nach Figurengewicht (Bauer leicht/hoch → Dame schwer/tief)

- Schlagen: zusätzlicher „Umfall"-Sound der geschlagenen Figur

- Springer: Sprungcharakter durch √5-Distanz

- Gelöst: aufsteigender Dreiklang

- Falsch: tiefer Buzz-Ton

### Weiteres

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

- **50.000 Puzzles** aus der [Lichess-Puzzle-Datenbank](https://database.lichess.org/#puzzles) — das entspricht ca. 1% der gesamten Lichess-Datenbank, ausgewählt nach Qualität

- **Lizenz:** CC0 (Public Domain)

- **Auswahlkriterien:** Popularity ≥ 50 (oberes Drittel), hohe Spielanzahl (NbPlays), Rating 400–3200, gleichmäßige Verteilung über alle Schwierigkeitsstufen, Rarity-Bonus für seltene taktische Motive

- **Format:** `\["ID", "FEN", "Moves", Rating, "Themes"\]`


## Verwendung

### Als Spieler

Einfach die Seite öffnen — kein Download, keine Installation: 👉 **[bielefeldersk.de/personalpuzzles**](https://www.bielefeldersk.de/personalpuzzles)

### Auf der eigenen Vereinsseite einbinden

Die Datei `PP\_35.html` herunterladen und direkt auf dem eigenen Server ablegen oder in ein HTML-Embed-Fenster einfügen (z.B. Wix, Jimdo, WordPress).

### Lokal ausführen

```
PP\_35.html herunterladen → im Browser öffnen → fertig
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

Personal Puzzles wurde entwickelt von **Guido Gößling** vom **[Bielefelder SK von 1883 e.V.**](https://www.bielefeldersk.de/) — 

Fragen, Ideen, Verbesserungsvorschläge: [guido.goessling@web.de](mailto:guido.goessling@web.de)


## Versionsverlauf

| Version | Datum | Highlights |
| - | - | - |
| PP\_35 | 02.04.2026 | Settings-Persistenz, Figurenanzahl-Filter, Zurücksetzen-Button |
| PP\_34 | 03.03.2026 | Settings-Reorganisation, Bonuszeit, Farbauswahl, Erweiterte Einstellungen |
| PP\_33 | 28.02.2026 | State-Objekt-Refactoring (reviewState, analysisState, sfState) |
| PP\_32 | 20.02.2026 | Stockfish-Integration, Analyse-Modus, Eval-Bar |
| PP\_31 | 18.02.2026 | Deselect, Hint-Zuganzahl, Grid-Vorschau, Matt-Motive |
| PP\_30 | — | Daily Puzzle System + Widget |
| PP\_24 | — | 50.000 Puzzles, Themen-Filter |



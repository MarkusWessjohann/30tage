# 30 Tage

**30 Tage** ist ein politisches Serious Game für den Browser. Du übernimmst die Rolle einer Spielfigur in einem fiktiven deutschen Dorf und versuchst, alltägliche Aufgaben zu bewältigen, während sich die öffentlichen Institutionen im Ort unter dem Einfluss einer simulierten politischen Programmatik verändern.

## Ausprobieren

Das Spiel kann direkt im Browser gespielt werden:

**[30 Tage starten](https://markuswessjohann.github.io/30tage/)**

Die Web-Version ist für Desktop-Browser ausgelegt. Eine Maus wird für die Interaktion empfohlen. Die Spielfigur kann zusätzlich mit `W`, `A`, `S` und `D` bewegt werden.

## Spielidee

Im Verlauf eines Spieldurchlaufs bewegst du dich durch das Dorf, besuchst Institutionen und erledigst Aufgaben. Dabei musst du unter anderem mit folgenden Faktoren umgehen:

- Geld und Gesundheit
- täglich neu zugewiesene Aufgaben und die Morgenpost
- Dialoge mit unterschiedlichen Entscheidungen und Ausweichlösungen
- sich verschlechternde Institutionen
- Naturereignisse und weitere politische Folgen
- persönliche Merkmale, die Aufgabenvarianten beeinflussen können

Das Spiel hat kein Highscore-Ziel. Am Ende steht ein Reflexionsmoment über die Auswirkungen politischer Entscheidungen und das eigene Wahlverhalten.

## Steuerung

| Eingabe | Funktion |
|---|---|
| Linksklick | Orte und Personen auswählen, Dialoge bedienen |
| `W` / `A` / `S` / `D` | Spielfigur direkt bewegen |

## Entwicklung

Das Spiel wird mit [Godot](https://godotengine.org/) und GDScript entwickelt. Das Projekt liegt im Verzeichnis `game/`.

### Voraussetzungen

- Godot 4.7 oder eine kompatible Godot-4-Version
- Git

Die verwendete Engine-Version ist im Projekt in `game/project.godot` hinterlegt. Für das lokale Spielen und Entwickeln wird die Datei `game/project.godot` im Godot-Editor geöffnet.

### Lokal starten

1. Repository klonen:

   ```bash
   git clone https://<ToDo>/<ToDo>.git
   cd afd
   ```

2. `game/project.godot` im Godot-Editor importieren bzw. öffnen.
3. Das Projekt mit **Run Project** starten.

Der Web-Build liegt als separates Git-Submodul unter `game/Build/Web/` und wird über GitHub Pages veröffentlicht.

## Projektstruktur

```text
game/
├── assets/       # Grafiken und Audio
├── autoloads/    # Globaler Spielzustand, Events und Logging
├── resources/    # Daten für Aufgaben, Dialoge, Institutionen und Balancing
├── scenes/       # Hauptszene, Dorfkarte, Dialoge und UI
└── systems/      # Tageszyklus, Aufgabenzuweisung, Wetter und Eskalation
```

Weitere Projekt- und Architekturentscheidungen sind in [`_bmad-output/game-architecture.md`](_bmad-output/game-architecture.md) dokumentiert.

## Quellenbasierte Analyse

Die Spielinhalte und politischen Folgen beziehen sich auf die quellenbasierte Auswertung im Verzeichnis [`afd-analyse/`](afd-analyse/). Dort werden Aussagen aus Parteidokumenten und öffentlich dokumentierten Quellen gesammelt, kategorisiert und politikwissenschaftlich eingeordnet.

Die Analyse kennzeichnet ausdrücklich, dass ihre Ampel-Einordnung eine Bewertung dieser Analyse und kein Gerichtsurteil ist. Details zur Methodik und zu den verwendeten Quellen stehen in [`afd-analyse/README.md`](afd-analyse/README.md).

## Status

Die aktuell konfigurierte Projektversion ist `0.9.1`. Das Spiel befindet sich in aktiver Entwicklung.

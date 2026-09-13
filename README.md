# PlanIt

Whiteboard als Claude-Artifact zum Skizzieren von Software (Bildschirme, Datenmodelle,
Abläufe) und zur Übergabe an Claude. Eine einzige HTML-Datei, keine Abhängigkeiten.

## Die Datei holen

Aktuelle Fassung direkt herunterladen:

```
https://raw.githubusercontent.com/luishindelang/planit/main/code/planit.html
```

Oder das Repo klonen und später mit `git pull` nachziehen:

```bash
git clone https://github.com/luishindelang/planit.git
```

Die Fassungsnummer steht in der Kopfzeile der Seite und in `code/planit.html` (`FASSUNG`).

## Eigenes Brett veröffentlichen

Claude (Claude Code) die Datei geben und sagen: *„veröffentliche das als Artifact mit
`capabilities {db:{}}`“*. Es entsteht ein eigenes Brett mit eigenem Speicher. Details, das
Datenschema und alle Regeln stehen in `CLAUDE.md`.

## Skills für Claude Code

Die drei Skills in `skills/` nach `~/.claude/skills/` kopieren (je ein Ordner mit `SKILL.md`):

- `planit-lesen` — ein Brett auslesen, als Markdown oder als Spezifikation
- `planit-schreiben` — Elemente, Pfeile, Reiter, Bausätze auf ein Brett schreiben
- `planit-veroeffentlichen` — Bretter anlegen und aktualisieren (braucht daneben eine eigene
  `bretter.json` mit den eigenen Brett-URLs; die ist bewusst nicht im Repo)

## Struktur

- `code/planit.html` — die eine Quelle, zugleich die Datei, die weitergegeben wird
- `code/undeklariert-pruefen.js` — Prüfskript (Zuweisungen an nie deklarierte Namen)
- `CLAUDE.md`, `PLAN.md` — Verfassung, Code-Landkarte, Datenschema, Plan und Historie
- `artefakte/` — Prüfprotokolle und alte Patch-Skripte

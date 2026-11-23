# otopark – Linkseite

Statische Seite ohne Build-Schritt. Alles, was online gehen soll, liegt in diesem Ordner.

## Inhalt

- `index.html` – die Linkseite (Links stehen im Block „LINKS BEARBEITEN“)
- `logo.webp` – euer Logo als Maske, die Farbe setzt die Seite selbst
- `bilder/` – kleine Bilder rechts neben den Links (aktuell Platzhalter aus dem Logo)
- `fonts/jetbrains-mono.woff2` – Schrift (JetBrains Mono), lokal eingebunden (kein Google-Fonts-Abruf)
- `impressum.html`, `datenschutz.html` – Gerüste, Platzhalter in [eckigen Klammern] ausfüllen
- `favicon.svg` – Symbol im Browser-Tab

## Links ändern

In `index.html` bei jedem Link `href="…"` (Ziel) und den Text in `<span class="txt">…</span>` anpassen.
Neue Links einfach als weitere Zeile darunter kopieren.
Logo- und Linkfarben stehen im Skript unter `COLORS`. Alle Links haben eine gemeinsame Farbe daraus, die immer eine andere ist als die des Logos.
Bild neben einem Link: `<img class="thumb" src="bilder/name.jpg" alt="" width="240" height="240">` vor `</a>` einfügen.

## Online stellen mit GitHub Pages (kostenlos)

1. Öffentliches Repository `otopark.github.io` in der GitHub-Organisation „otopark“ anlegen (leer).
2. In diesem Ordner:
   git init && git switch -c main && git add . && git commit -m "Linkseite"
   git remote add origin https://github.com/otopark/otopark.github.io.git
   git push -u origin main
3. Repository → Settings → Pages → Deploy from a branch → main, / (root) → Save.
4. Eigene Domain: erst unter Settings → Pages eintragen, dann beim Domain-Anbieter
   A-Einträge auf 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   und für www einen CNAME auf otopark.github.io. Danach „Enforce HTTPS“ anhaken.

Änderungen: bearbeiten, `git commit -am "…"`, `git push` – nach etwa einer Minute online.

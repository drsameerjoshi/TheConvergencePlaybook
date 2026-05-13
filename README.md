# The Convergence Playbook — Vollständige Website (Self-Contained)

Offizielle Landing Page für **"The Convergence Playbook"** von Prof. Dr. Sameer Joshi und Thorsten Buehrmann.

Diese Version ist **vollständig autark** — alle Bilder, Schriften und Skripte sind lokal enthalten. Die Website funktioniert ohne externe Abhängigkeiten (einzige Ausnahme: das Wistia-Video benötigt eine Internetverbindung zum Streamen).

---

## Dateistruktur

```
TheConvergencePlaybook_Website/
├── index.html              ← Hauptseite
├── README.md               ← Diese Anleitung
├── assets/
│   ├── index-*.css         ← Styles (Tailwind CSS)
│   └── index-*.js          ← React App (gebündelt)
├── fonts/
│   ├── fonts.css           ← Font-Face Definitionen
│   ├── inter_*.woff2       ← Inter Font (Body-Text)
│   ├── spacegrotesk_*.woff2 ← Space Grotesk (Headlines)
│   └── jetbrainsmono_*.woff2 ← JetBrains Mono (Code/Labels)
└── images/
    ├── hero_bg.webp        ← Hero Hintergrundbild
    ├── problem_bg.webp     ← Problem-Sektion Hintergrund
    ├── manifold_bg.webp    ← Framework-Sektion Hintergrund
    ├── cta_bg.webp         ← CTA-Sektion Hintergrund
    ├── book_cover.webp     ← Buchcover
    ├── sameer_portrait.png ← Portrait Sameer Joshi
    ├── thorsten_portrait.png ← Portrait Thorsten Buehrmann
    ├── quasality_logo.png  ← Quasality.AI Logo
    ├── manifold_diagram.png ← Sovereign Manifold Diagramm
    └── thumbnail.webp      ← YouTube/Video Thumbnail
```

---

## Schnellstart

### Option 1: Lokale Vorschau (sofort testen)

Die einfachste Methode — Python ist auf den meisten Systemen vorinstalliert:

```bash
cd TheConvergencePlaybook_Website
python3 -m http.server 8080
```

Dann im Browser öffnen: **http://localhost:8080**

Alternativ mit Node.js:

```bash
cd TheConvergencePlaybook_Website
npx serve .
```

**Hinweis:** Die `index.html` direkt per Doppelklick öffnen funktioniert NICHT zuverlässig, da Browser lokale Dateizugriffe einschränken. Bitte immer einen lokalen Webserver verwenden.

### Option 2: Auf eigenem Webserver deployen

1. Alle Dateien und Ordner per FTP/SFTP auf den Webserver hochladen
2. Sicherstellen, dass `index.html` im Root-Verzeichnis der Domain liegt
3. Die Ordnerstruktur (`assets/`, `fonts/`, `images/`) muss beibehalten werden

### Option 3: Hosting-Dienste (Netlify, Vercel, etc.)

1. Den gesamten Ordner als ZIP bei Netlify/Vercel hochladen
2. Oder per Git-Repository deployen
3. Keine Build-Schritte nötig — alles ist bereits gebaut

---

## Was lokal enthalten ist

| Kategorie | Anzahl | Beschreibung |
|-----------|--------|--------------|
| Bilder | 10 | Alle Hintergründe, Portraits, Logos, Diagramme |
| Schriften | 16 | Inter, Space Grotesk, JetBrains Mono (alle Gewichte) |
| CSS | 1 | Tailwind CSS + Custom Theme (Quantum Noir) |
| JavaScript | 1 | React App komplett gebündelt |

## Einzige externe Abhängigkeit

Das **Wistia-Video** ("The Sovereign Choice") wird von Wistia gestreamt und benötigt eine Internetverbindung. Die Wistia Player-Scripts werden ebenfalls extern geladen. Falls kein Internet verfügbar ist, wird das Video einfach nicht angezeigt — der Rest der Seite funktioniert normal.

---

## Domain-Konfiguration

Für die Nutzung mit **TheConvergencePlaybook.com**:

1. DNS A-Record oder CNAME auf den Webserver zeigen lassen
2. SSL-Zertifikat einrichten (z.B. via Let's Encrypt)
3. Alle Dateien in das Web-Root-Verzeichnis hochladen
4. Sicherstellen, dass die Ordnerstruktur erhalten bleibt

---

## Technologie-Stack

- **Frontend**: React 19 + Tailwind CSS 4
- **Build**: Vite (bereits gebaut, kein Build nötig)
- **Schriften**: Google Fonts (lokal eingebettet als WOFF2)
- **Video**: Wistia Player (extern gestreamt)
- **Animationen**: Reine CSS-Animationen + Intersection Observer

---

© 2026 TheConvergencePlaybook.com — Alle Rechte vorbehalten.

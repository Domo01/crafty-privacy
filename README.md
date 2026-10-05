# Crafty Privacy Site

Statische Datenschutz-Website für **Crafty** (CA-Discord-System).

Keine Build-Pipeline. Keine React-/Next-/Node-Abhängigkeit.
Nur HTML + CSS — direkt über GitHub Pages hostbar.

## 1. Zweck

Öffentlich lesbare, schlicht formatierte Datenschutzhinweise für den privaten
Minecraft-/Discord-Server. Inhaltlich abgestimmt auf den aktuellen Code-Stand
und die internen Dokumente:

- `../PRIVACY_DATA_MAP.md`
- `../legal/privacy-policy-de.md`

Diese Seite ersetzt keine Rechtsberatung.

## 2. Lokale Vorschau

Im Ordner `privacy-site/` die Datei `index.html` im Browser öffnen
(Doppelklick oder „Open with Live Server“).

Relative Assets:

```text
./style.css
```

## 3. GitHub Pages Deployment (empfohlen)

**Nicht** das komplette `CA-DISCORD-SYSTEM`-Repository öffentlich machen.

Empfohlen: eigenes öffentliches Repository nur für diese Privacy-Website, z. B.:

```text
crafty-privacy/
```

### Variante A – eigener Repo-Inhalt

1. Neues öffentliches GitHub-Repository anlegen (z. B. `crafty-privacy`).
2. Inhalt von `privacy-site/` als Root des neuen Repos kopieren:
   - `index.html`
   - `style.css`
   - `robots.txt`
   - `.nojekyll`
   - optional dieses `README.md`
3. In GitHub: **Settings → Pages**
   - Source: Deploy from a branch
   - Branch: `main` (oder `master`)
   - Folder: `/ (root)`
4. Speichern und warten, bis die Seite live ist.

### Variante B – Unterordner im gleichen Repo

Nur sinnvoll, wenn das Repo ohnehin öffentlich ist (für Crafty i. d. R. **nicht** empfohlen).

Dann in Pages den `/privacy-site` Ordner bzw. passende GitHub-Actions-Konfiguration nutzen.

## 4. Notwendige Platzhalter

Vor Veröffentlichung ersetzen:

| Platzhalter | Bedeutung |
|---|---|
| `[KONTAKT_EMAIL]` | Echte Kontaktadresse für Datenschutzanfragen |

Keine Klarnamen oder Privatanschriften automatisch eintragen.

## 5. URL im Discord Bot eintragen

Nach dem Deploy z. B.:

```text
https://USERNAME.github.io/crafty-privacy/
```

Dann im Bot:

```env
PRIVACY_POLICY_URL=https://USERNAME.github.io/crafty-privacy/
```

Zusätzlich im Discord Developer Portal:

**Application → General Information / App Information → Privacy Policy URL**

dieselbe URL eintragen.

## 6. Was diese Seite bewusst nicht enthält

- kein Impressum mit Klarname/Adresse
- keine Tracking-/Analytics-Skripte
- keine Cookies / LocalStorage
- keine externen Fonts / CDNs / Widgets
- keine Secrets, Tokens, echten User-IDs oder UUIDs

## 7. TODOs vor öffentlicher / kommerzieller Nutzung

- `[KONTAKT_EMAIL]` durch eine echte Adresse ersetzen
- Rechtsgrundlage vor einer öffentlichen / kommerziellen Nutzung rechtlich prüfen
- Wenn Crafty, Discord oder Minecraft Server später öffentlich angeboten,
  kommerzialisiert oder wesentlich über den privaten Freundeskreis hinaus
  betrieben werden: Anbieterkennzeichnung / Impressum erneut prüfen
- Betreiberangaben / Verantwortlicher ggf. ergänzen (siehe HTML-Source-Comment)

## 8. Dateien

```text
privacy-site/
├── index.html
├── style.css
├── README.md
├── robots.txt
└── .nojekyll
```

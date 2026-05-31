# ABA V2 — Bestandsaufnahme Elektroanlagen

Progressive Web App (PWA) für die Bestandsaufnahme von Elektroanlagen.  
Installierbar auf **iOS**, **Android** und **Windows**.

## Features

- 📂 **CSV-Import** — Auftraggeber + Objekt-Adressen (Format A einfach / Format B vollständig)
- 🔍 **Adress-Autocomplete** — Suche in geladenen CSV-Daten, Auftraggeber wird automatisch befüllt
- 🏢 **Mehrfamilienhaus-Logik** — Gemeinschaftsbereiche + einzelne Wohnungen auswählbar
- 🪜 **Erweitertes Treppenhaus** — bis 8 Etagen, Notlicht, RZL, Rauchwarnmelder, Aufzug
- 📄 **PDF-Export** — Vollständiges Protokoll mit Briefkopf, Tabellen, Seitennummern
- 📴 **Offline-fähig** — Service Worker cached alle Inhalte

---

## Auf GitHub Pages veröffentlichen

1. Repository anlegen: `ABA-v2`
2. Alle Dateien in den `main`-Branch pushen
3. **Settings → Pages → Source: Deploy from branch → main / root**
4. App erreichbar unter: `https://DEIN-USERNAME.github.io/ABA-v2/`

---

## PWA installieren

### iOS (Safari)
1. App-URL in Safari öffnen
2. Teilen-Symbol antippen → **„Zum Home-Bildschirm"**

### Android (Chrome)
1. App-URL in Chrome öffnen
2. Banner „App installieren" antippen — oder Menü → **„App installieren"**

### Windows (Chrome / Edge)
1. App-URL öffnen
2. Adressleiste: Install-Symbol antippen oder Menü → **„App installieren"**

---

## CSV-Formate

### Format A — Einfach (von Hausverwaltung geliefert)
```
Auftraggeber;Adresse
Müller GmbH;Hauptstraße 12, 10117 Berlin
Schmidt & Co.;Bahnhofstr. 5, 22041 Hamburg
```

### Format B — Vollständig (mit Wohnungsbezeichnungen)
```
Auftraggeber;Adresse;Etagen;Wohnungen
Müller GmbH;Hauptstraße 12, 10117 Berlin;4;EG-Links|EG-Rechts|1OG-Links|1OG-Rechts
```

---

## Dateistruktur
```
ABA-v2/
├── index.html       ← Komplette App (eine Datei)
├── manifest.json    ← PWA-Manifest
├── sw.js            ← Service Worker (Offline)
├── icon-192.png     ← App-Icon 192×192 px
├── icon-512.png     ← App-Icon 512×512 px
└── README.md
```

---

## Icons erstellen

Die Icons (`icon-192.png`, `icon-512.png`) müssen noch erstellt werden.  
Empfehlung: [PWA Asset Generator](https://progressier.com/pwa-icons-and-ios-splash-screen-generator) oder ein beliebiges Tool.  
Quadratisches Logo in blau (#1a56db) verwenden — passt zum App-Design.

---

## Offene Punkte (Roadmap)
- [ ] Firmenname im PDF konfigurierbar
- [ ] Unterschriftenfelder im PDF
- [ ] Wohnungsbezeichnungen aus CSV editierbar
- [ ] Dexie.js-Persistenz (Daten bleiben nach App-Neustart)

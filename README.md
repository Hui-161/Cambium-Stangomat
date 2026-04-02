# Cambium → Stangomat

**CSV-Import-Vorbereitung für den Stangomat** — direkt im Browser, keine Installation, keine externen Abhängigkeiten.

🔗 **[→ Web-App direkt öffnen](https://hui-161.github.io/cambium-stangomat/)**

---

## Was macht das Tool?

Das Tool wandelt Cambium-Holzlisten (CSV) in das Stangomat-Importformat um — vollständig lokal im Browser, ohne Server, ohne Datenweitergabe.

### Funktionen

- **CSV-Import** — Drag & Drop oder Dateiauswahl; erkennt automatisch Semikolon, Komma oder Tab als Trennzeichen sowie UTF-8 und Windows-1252 Encoding
- **Automatische Spaltenzuordnung** — erkennt Felder wie Schnittklasse, Breite, Höhe, Länge, Anzahl, Bauteilnr., Paket
- **KVH-Verarbeitung** — Längen auf volle mm auf- oder abrunden; Hölzer unter 1500 mm als Fehler ausgeben, auf 1500 mm aufrunden oder beibehalten
- **BSH-Verarbeitung** — Systemlängen automatisch zuweisen oder BSH-Hölzer in separate CSV ausleiten
- **Manuelle Bearbeitung** — alle Felder direkt in der Tabelle editierbar
- **Paketverwaltung** — Bauteile in Pakete gruppieren, umbenennen, zusammenführen
- **Fehler & Warnungen** — übersichtlich aufgelistet, fehlerhafte Zeilen als separate Industrie-Bestellung exportierbar
- **Exakte Stiele** — fasst Hölzer mit gleichem Querschnitt (b/h und h/b werden gleichgestellt) und exakt gleicher Länge zusammen; Stückzahlen werden addiert, alle Bauteilnummern in den Anmerkungen gesammelt

### Export

| Datei | Inhalt |
|---|---|
| `Stangomat_Import.csv` | Normaler Stangomat-Import |
| `Exakte_Stiele_Import.csv` | Zusammengefasste Exakt-Stiele |
| `Stangomat_Kombiniert_Import.csv` | Stangomat-Export + Exakte Stiele in einer Datei |
| `Industrie_Bestellung.csv` | Fehlerhafte Zeilen im Original-Format |
| `BSH_Sonder_Export.csv` | BSH-Sonderlängen separat |

Alle Dateien: **Windows-1252 Encoding, Semikolon-getrennt, CRLF** — exakt das Format, das Stangomat erwartet.

---

## Verwendung

1. Seite öffnen → CSV-Datei hochladen (Drag & Drop oder Klick)
2. Spaltenzuordnung prüfen → „Zuordnung übernehmen & prüfen"
3. Fehler & Warnungen korrigieren
4. Optional: Pakete verwalten, Bauteile manuell bearbeiten
5. Tab **Export-Vorschau** → gewünschte CSV herunterladen

---

## Lokale Nutzung (offline)

Die gesamte App ist eine **einzelne HTML-Datei** ohne externe Abhängigkeiten — läuft direkt im Browser:

```bash
# Datei herunterladen
curl -L -o Cambium_Stangomat.html \
  https://raw.githubusercontent.com/DEIN-GITHUB-NAME/cambium-stangomat/main/Cambium_-_Stangomat.html

# Dann einfach doppelklicken — fertig.
```

Oder Repository klonen:

```bash
git clone https://github.com/DEIN-GITHUB-NAME/cambium-stangomat.git
cd cambium-stangomat
# Cambium_-_Stangomat.html im Browser öffnen
```

---

## Datenschutz & IT-Sicherheit

- ✅ **Keine externen Skripte** — vollständig offline-fähig
- ✅ **Keine Datenübertragung** — alle Daten bleiben lokal im Browser
- ✅ **Kein Server** — statische HTML-Datei, kein Backend
- ✅ **Keine Installation** — läuft direkt im Browser

---

## Technisch

- Einzelne HTML-Datei (~1000 Zeilen)
- Vanilla JavaScript, kein Framework
- Kompatibel mit Chrome, Firefox, Edge, Safari

---

## Lizenz

MIT — frei verwendbar und anpassbar.

# Source of Funds Viewer

Eine **Single-Page-Applikation (SPA)** zum Visualisieren und Auswerten von Bitcoin-Transaktionsdaten als **Mittelherkunftsnachweis** – direkt im Browser, ohne Server und ohne Installation.

---

## 📋 Überblick

Der **Source of Funds Viewer** lädt eine CSV-Datei mit Bitcoin-Transaktionsdaten und stellt diese übersichtlich als Karten-Ansicht dar. Alle Daten werden lokal im Browser verarbeitet – es werden keine Daten an externe Server gesendet.

---

## 🚀 Funktionen

- **CSV-Import** per Datei-Upload (Trennzeichen `;`)
- **Automatisches Laden** einer Beispiel-Datei beim Start (siehe unten)
- **Gruppierung** von Transaktionen anhand der `transaction_id`
- **Jahresweise Darstellung** der Vorgänge
- **Suche** über alle oder einzelne Felder
- **Sortierung** nach beliebigen Spalten (auf-/absteigend)
- **Spalten ein-/ausblenden** mit Voreinstellungen
- **Hell- / Dunkel-Modus** (wird lokal gespeichert)
- **Verlinkung** zu Blockchain-Explorern für Transaktions-IDs und Adressen
- **Kaufzusammenfassung** je Jahr mit BTC- und Euro-Beträgen
- **Nachweise** als klickbare Dokument-Links (bis zu 12 Dokumente je Vorgang)

---

## 📁 Dargestellte Datenbereiche

Jede Transaktion/Ereignis wird in folgende Sektionen unterteilt:

| Sektion | Inhalt |
|---|---|
| **Informationen zur Transaktion** | Transaktions-ID, Gebühren, Adressen, Adresswerte |
| **Block-Informationen** | Blockhöhe, Blockhash |
| **Wallet-Infos** | Account-Nummer/-Name, Ableitungspfad, Extended Public Keys & Fingerprints |
| **Börsen-Daten** | Börsenname/-typ, BTC/EUR-Kurs, Gebühren, Beträge |
| **Beschreibungen** | Eigentümer- und Behördenbeschreibungen |
| **Nachweise** | Bis zu 12 verknüpfte Dokumente |

---

## 📄 Unterstützte Ereignistypen (`event`)

| Wert          | Bezeichnung                             |
|---------------|-----------------------------------------|
| `transaction` | Transaktion                             |
| `buy`         | Kauf                                    |
| `sell`        | Verkauf                                 |
| `deposit`     | Einzahlung                              |
| `receive`     | Empfangen einer Börsen-Auszahlung       |
| `gift`        | Geschenk / Freundschaftsprämie / Bonus  |

---

## 📂 Beispiel-Datei

Beim Start wird automatisch die Beispiel-Datei **`mittelherkunftsnachweis-beispiel.csv`** geladen, sodass die Anwendung sofort mit Beispieldaten befüllt ist.

Zusätzlich steht eine **Excel-Datei** (`mittelherkunftsnachweis-beispiel.xlsx`) bereit, die inhaltlich der Beispiel-CSV entspricht und als Vorlage zum Erstellen eigener Einträge genutzt werden kann.

---

## 🛠️ CSV erstellen

Zum Erstellen einer eigenen CSV-Datei im passenden Format stehen folgende Tools zur Verfügung:

- **Web-Anwendung:** [Transaction Collector Web](https://orangebitman.github.io/Transaction-Collector-Web/)
- **Desktop-Anwendung:** [Transaction Collector (GitHub)](https://github.com/OrangeBitman/Transaction-Collector)

> Die CSV-Datei muss Semikolon (`;`) als Trennzeichen verwenden und UTF-8-kodiert sein.

---

## 💻 Verwendung

1. `index.html` im Browser öffnen.
2. Die Beispiel-Datei wird automatisch geladen – **oder** oben rechts über **📁 CSV laden** eine eigene Datei auswählen.
3. Suche, Sortierung und Spaltenfilter nach Bedarf anpassen.
4. Mit dem Button **🌙 Dunkel / ☀️ Hell** zwischen den Themes wechseln.

---

## 📦 Projektstruktur

```text
.
├── index.html                            # Single-Page-App (gesamte Anwendung)
├── mittelherkunftsnachweis-beispiel.csv  # Beispiel-CSV-Datei
└── mittelherkunftsnachweis-beispiel.xlsx # Beispiel-Excel-Datei (entspricht der CSV)
```
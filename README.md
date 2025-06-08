
# Die Feiertage in Deutschland – Öffentliche API & Informationsportal

Willkommen im offiziellen GitHub-Repository zur **Feiertags-API** von [https://die-feiertage-in-deutschland.de](https://die-feiertage-in-deutschland.de).

Diese Plattform bietet zwei zentrale Angebote:

1. 🖥 **Informationsportal** – Nutzerfreundliche Website mit Kalendern, Feiertagsübersichten, Monats- und Bundeslandfilter.
2. 🔌 **REST-API-Zugang** – Für Entwickler:innen, die Feiertagsdaten strukturiert im JSON-Format abrufen möchten.

---

## 🔗 Hauptzugänge

| Bereich                  | Link                                                                 |
|--------------------------|----------------------------------------------------------------------|
| 🌐 Startseite            | [Zur Website](https://die-feiertage-in-deutschland.de)               |
| 🗓 Alle Feiertage        | [Feiertagsliste](https://die-feiertage-in-deutschland.de/feiertage) |
| 📅 Monatsübersicht       | [Monate](https://die-feiertage-in-deutschland.de/monate)            |
| 🧭 Bundesländerfilter    | [Bundesländer](https://die-feiertage-in-deutschland.de/bundeslaender)|
| 📡 Feiertags-API         | [API Tool](https://die-feiertage-in-deutschland.de/api_tool)        |

---

## 🧠 Über das Projekt

Dies ist ein **Open Source Projekt**, das mit **Oracle APEX** entwickelt wurde. Ziel ist es, eine zentrale Plattform für Feiertagsinformationen in Deutschland bereitzustellen – sowohl für Bürger:innen als auch für Entwickler:innen, die auf strukturierte Feiertagsdaten via REST-API zugreifen möchten.

Die Anwendung steht **kostenlos** zur Verfügung und darf gerne weiterverwendet, erweitert oder integriert werden. 

Ich freue mich über **Feedback**, **Verbesserungsvorschläge** oder **Pull Requests** von der Community.

---

## 📸 Screenshots & Einblicke

### 🏠 Startseite
Auf der **Startseite** erhält man eine kompakte Übersicht über alle besonderen Tage – ob **gesetzliche Feiertage**, **Ereignistage** oder **festliche Anlässe**. Man kann direkt filtern und sieht sofort, ob **heute ein Feiertag** ist oder **welcher besondere Tag als Nächstes ansteht**.

🔗 Zur Startseite: [https://die-feiertage-in-deutschland.de](https://die-feiertage-in-deutschland.de)

[![Startseite](https://prod-apache.shsoftwaresolution.de/public_website_data/data/feiertage/app_image/startseite.avif)](https://die-feiertage-in-deutschland.de)

---

### 📡 API Tool
Das **API Tool** ermöglicht es, REST-Endpunkte dynamisch zu testen. Nutzer:innen können flexibel wählen, wie sie die Feiertage abrufen möchten – z. B. nur nach Jahr, nach Jahr + Monat, nach Jahr + Bundesland oder sogar kombiniert mit Kategorie-Filtern.

Man baut sich seinen persönlichen API-Link direkt zusammen und erhält die Ergebnisse im JSON-Format – **ideal für Entwickler:innen, Integrationen oder Automatisierungen**.

🔗 Zum API-Tool: [https://die-feiertage-in-deutschland.de/api_tool](https://die-feiertage-in-deutschland.de/api_tool)

![API Tool](https://prod-apache.shsoftwaresolution.de/public_website_data/data/feiertage/app_image/api.avif)


---

### 🧭 Bundesländer
Auf der Seite **Bundesländer** findet man eine vollständige Übersicht über alle 16 Bundesländer Deutschlands.

Hier kann man gezielt filtern, **welche Feiertage in welchem Bundesland** gelten – inklusive Jahresauswahl und direkter Vergleichsmöglichkeit.

🔗 Zur Übersicht: [https://die-feiertage-in-deutschland.de/bundeslaender](https://die-feiertage-in-deutschland.de/bundeslaender)

![Bundesländer](https://prod-apache.shsoftwaresolution.de/public_website_data/data/feiertage/app_image/bundeslaender.avif)

---

### 📅 Monatsansicht
In der **Monatsansicht** bekommt man eine strukturierte Übersicht aller Monate des Jahres. 

Man sieht sofort, **welche Feiertage es in welchem Monat** gibt – gefiltert nach **Bundesland**, **Jahr** und **Kategorie**. Ideal für eine gezielte Monatsplanung oder zur Integration in Kalenderdienste.

🔗 Zur Monatsübersicht: [https://die-feiertage-in-deutschland.de/monate](https://die-feiertage-in-deutschland.de/monate)

![Monate](https://prod-apache.shsoftwaresolution.de/public_website_data/data/feiertage/app_image/monate.avif)


---

## 🎉 Feiertagsübersicht
Hier findet man eine vollständige Liste **aller Feiertage**, kategorisiert nach gesetzlichen Feiertagen, festlichen Tagen und Ereignistagen.

Man kann sehen, **wann ein bestimmter Feiertag stattfindet** – bis zu 10 Jahre in die Vergangenheit und Zukunft. Zusätzlich gibt es zu jedem Feiertag eine **ausführliche Beschreibung** mit kulturellem Kontext.

🔗 Direktlink: [https://die-feiertage-in-deutschland.de/feiertage](https://die-feiertage-in-deutschland.de/feiertage)

![Feiertage](https://prod-apache.shsoftwaresolution.de/public_website_data/data/feiertage/app_image/feiertage.avif)

---

## 🔌 API-Nutzung

### Basis-Endpunkt

Alle Endpunkte liefern strukturierte JSON-Daten:

```
GET /api/year/{year}
```

Beispiel:
```
https://die-feiertage-in-deutschland.de/ords/feiertage/api/year/2025
```

### Weitere Endpunkte

- `/api/state/{year}/{state}` → Feiertage für ein Bundesland
- `/api/month/{year}/{month}` → Feiertage eines Monats
- `/api/category/{year}/{category}/{state}` → Gefiltert nach Kategorie & Region

---

## 📂 Rückgabeformat (Beispiel)

```json
{
  "items": [
    {
      "holiday_name": "Neujahr",
      "holiday_date": "01.01.2025",
      "holiday_day": 1,
      "holiday_month_number": 1,
      "holiday_month_name": "Januar",
      "holiday_year": 2025,
      "applicable_states": "Alle Bundesländer",
      "category_code": "PUBLIC",
      "category_label": "Gesetzlicher Feiertag",
      "holiday_description": "Der erste Tag des Jahres markiert den Beginn eines neuen Kalenderjahres..."
    }
  ]
}
```

---

## 📬 Kontakt

Fragen oder Anregungen? Bitte ein Issue öffnen oder über die Website das Kontaktformular nutzen.

> Bereitgestellt von [shsoftwaresolution.de](https://shsoftwaresolution.de) – mit Fokus auf Datenqualität & Nutzerfreundlichkeit.

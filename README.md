
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

Die Website wurde manuell erstellt – **nicht mit Hilfe von KI**, sondern mit viel Sorgfalt und Fachwissen entwickelt, um Nutzern einen einfachen Zugang zu sämtlichen Feiertagen Deutschlands zu ermöglichen. Die REST-API ist ein Zusatzangebot für Entwickler:innen.

---

## 📸 Screenshots & Einblicke

### 🏠 Startseite
![Startseite](https://prod-apache.shsoftwaresolution.de/public_website_data/data/feiertage/app_image/startseite.avif)

---

### 📡 API Tool
Hier kann man REST-Endpunkte dynamisch ausprobieren und direkt filtern.
![API Tool](https://prod-apache.shsoftwaresolution.de/public_website_data/data/feiertage/app_image/api.avif)

---

### 🧭 Bundesländer
Filterbare Ansicht nach einzelnen Bundesländern.
![Bundesländer](https://prod-apache.shsoftwaresolution.de/public_website_data/data/feiertage/app_image/bundeslaender.avif)

---

### 📅 Monatsansicht
Kalenderansicht der Feiertage sortiert nach Monaten.
![Monate](https://prod-apache.shsoftwaresolution.de/public_website_data/data/feiertage/app_image/monate.avif)

---

### 🎉 Feiertagsübersicht
Alle besonderen Tage, geordnet nach Kategorien: gesetzlich, festlich, historisch.
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

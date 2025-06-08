# 🇩🇪 Feiertags-API Deutschland

Diese API stellt **alle gesetzlichen Feiertage, Festtage und besonderen Ereignisse in Deutschland** als strukturierte, filterbare JSON-Daten zur Verfügung – **kostenfrei** über eine öffentliche REST-Schnittstelle.

Die gesamte Lösung wurde von Hand entwickelt – **nicht von künstlicher Intelligenz generiert**, sondern sorgfältig kuratiert und implementiert.

---

## 🔗 Offizielle Projektseite

👉 **[API-Webseite ansehen](https://die-feiertage-in-deutschland.de/api_tool)**  
Hier findest du eine vollständige Anleitung zur Nutzung der REST-Endpunkte sowie interaktive UI-Komponenten zur API-Konfiguration.

---

## 🌐 Direktzugriff auf alle Inhalte

- 🌍 **Startseite mit Vollfilter**  
  [https://die-feiertage-in-deutschland.de](https://die-feiertage-in-deutschland.de)

- 📍 **Feiertage nach Bundesländern**  
  [https://die-feiertage-in-deutschland.de/bundeslaender](https://die-feiertage-in-deutschland.de/bundeslaender)

- 📆 **Feiertage nach Monaten**  
  [https://die-feiertage-in-deutschland.de/monate](https://die-feiertage-in-deutschland.de/monate)

- 🎉 **Alle Feiertage aufgelistet**  
  [https://die-feiertage-in-deutschland.de/feiertage](https://die-feiertage-in-deutschland.de/feiertage)

---

## 🛠️ Verfügbare API-Endpunkte

| Methode | Endpunkt | Beschreibung |
|--------|----------|--------------|
| `GET` | `/api/year/{year}` | Alle Feiertage für ein bestimmtes Jahr |
| `GET` | `/api/month/{year}/{month}` | Feiertage eines bestimmten Monats |
| `GET` | `/api/state/{year}/{state}` | Feiertage eines bestimmten Bundeslands |
| `GET` | `/api/category/{year}/{category}/{state}` | Kombinierter Filter: Jahr, Kategorie(n) und Bundesland/Bundesländer |

---

## 📌 Beispielaufrufe

```bash
GET https://die-feiertage-in-deutschland.de/ords/feiertage/api/year/2025
GET https://die-feiertage-in-deutschland.de/ords/feiertage/api/month/2025/06
GET https://die-feiertage-in-deutschland.de/ords/feiertage/api/state/2025/BY:BW
GET https://die-feiertage-in-deutschland.de/ords/feiertage/api/category/2025/public:event/all





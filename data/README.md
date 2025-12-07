# Daten-Dateien für die Website

Diese Dateien enthalten die Daten, die auf der Website angezeigt werden. Sie können separat bearbeitet werden, ohne die HTML-Datei zu ändern.

## Dateien

### `operations.json` - Einsatzberichte
Enthält Informationen über vergangene Einsätze.

**Struktur:**
```json
{
  "operations": [
    {
      "id": 1,
      "title": "Operation Name",
      "date": "2025-12-01",
      "type": "Kampfeinsatz",
      "description": "Beschreibung des Einsatzes",
      "participants": 24,
      "status": "Abgeschlossen",
      "image": "URL zum Bild"
    }
  ]
}
```

**Felder:**
- `id`: Eindeutige ID (Nummer)
- `title`: Name der Operation
- `date`: Datum im Format YYYY-MM-DD
- `type`: Typ des Einsatzes (z.B. "Kampfeinsatz", "Patrouille")
- `description`: Beschreibung des Einsatzes
- `participants`: Anzahl der Teilnehmer
- `status`: Status (z.B. "Abgeschlossen", "Geplant")
- `image`: URL zu einem Bild (optional)

### `availability.json` - Verfügbarkeiten
Enthält die Verfügbarkeitsstatus aller MOS/AFSC Positionen.

**Struktur:**
```json
{
  "usArmy": [
    {
      "code": "11A",
      "name": "Infantry Officer",
      "description": "Beschreibung",
      "status": "green",
      "statusText": "Offen"
    }
  ],
  "usAirForce": [
    {
      "code": "11F",
      "name": "Fixed Wing Fighter Pilot",
      "description": "Beschreibung",
      "status": "green",
      "statusText": "Offen"
    }
  ]
}
```

**Status-Werte:**
- `"green"`: Offen
- `"yellow"`: Auf Anfrage / Teilweise offen
- `"red"`: Geschlossen / Nur erfahrene Spieler

**statusText:** Der Text, der angezeigt wird (z.B. "Offen", "Geschlossen", "Nur erfahrene Spieler")

## Bearbeitung

1. Öffnen Sie die entsprechende JSON-Datei in einem Texteditor
2. Bearbeiten Sie die Daten (achten Sie auf korrekte JSON-Syntax!)
3. Speichern Sie die Datei
4. Die Website lädt die Daten automatisch beim nächsten Seitenaufruf

**Wichtig:** 
- Verwenden Sie immer korrekte JSON-Syntax (Kommas, Anführungszeichen)
- Testen Sie die JSON-Datei mit einem JSON-Validator, bevor Sie sie speichern
- Die Dateien müssen im `data/` Ordner bleiben








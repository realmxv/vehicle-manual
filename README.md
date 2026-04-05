# Fahrzeug-Bedienungsanleitung

Strukturierte Bedienungsanleitung für Reisemobile — JSON-basiert. Kategorien: Fahrzeug, Wallout, Technik, Hydraulik, Fluessigkeiten, Heizung, Klima, Plateau, Abfahrtskontrolle. Wird von der App als JSON geladen.

## Struktur

```
vehicle-manual/
├── index.json          # Hauptindex: Kategorien, Modelle, Metadaten
├── schema.json         # JSON-Schema für Validierung
├── entries/            # Alle Anleitungs-Eintraege
│   ├── fahrzeug/
│   ├── wallout/
│   ├── technik/
│   ├── hydraulik/
│   ├── fluessigkeiten/
│   ├── heizung/
│   ├── klima/
│   ├── plateau/
│   └── abfahrtskontrolle/
└── images/             # Bilder (per URL von der App geladen)
```

## Versionierung

Jeder Eintrag hat `validFrom` (YYYY-MM), `validUntil` (YYYY-MM oder null), und `models` (Array). Die App zeigt nur passende Eintraege an.

## Section-Typen

heading, text, steps, checklist, warning, info, image

## Bilder

Bilder in images/ speichern. Die App laedt sie ueber die GitHub Raw-URL.

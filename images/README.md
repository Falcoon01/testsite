# Bilder-Ordnerstruktur

Diese Ordnerstruktur organisiert alle Bilder der Website für lokale Einbettung.

## Ordnerstruktur

```
images/
├── operations/      # Bilder für Einsatzberichte (operations.json)
├── availability/    # Bilder für Rollen-Spezifizierungen (availability.json)
├── slider/          # Bilder für den Hauptslider (index.html)
├── logos/           # Logos (Army, USAF, etc.)
└── misc/            # Sonstige Bilder (z.B. A-10 Warthog)
```

## Verwendung

### Operations-Bilder (`images/operations/`)
Bilder für die Einsatzberichte. Benennung: `operation-{id}-{index}.{ext}`

**Beispiel:**
- `operation-1-1.png` - Erstes Bild der Operation 1
- `operation-2-1.jpg` - Erstes Bild der Operation 2
- `operation-2-2.jpg` - Zweites Bild der Operation 2

**In `data/operations.json` verwenden:**
```json
"images": [
  "images/operations/operation-1-1.png"
]
```

### Availability-Bilder (`images/availability/`)
Bilder für die Rollen-Spezifizierungen. Benennung: `{code}.{ext}`

**Beispiel:**
- `11B.jpg` - Bild für Infantryman (11B)
- `1Z3X1.jpg` - Bild für TACP (1Z3X1)

**In `data/availability.json` verwenden:**
```json
"image": "images/availability/11B.jpg"
```

### Slider-Bilder (`images/slider/`)
Bilder für den Hauptslider. Benennung: `slider-{index}.{ext}`

**Beispiel:**
- `slider-1.jpg`
- `slider-2.jpg`
- `slider-3.jpg`

**In `index.html` verwenden:**
```html
<img src="images/slider/slider-1.jpg" class="active" alt="Slider Bild 1">
```

### Logos (`images/logos/`)
Logos für Army, USAF, etc. Benennung: `{name}.{ext}`

**Beispiel:**
- `army-logo.png`
- `usaf-logo.png`

**In `index.html` verwenden:**
```html
<img src="images/logos/army-logo.png" alt="Army Logo" class="slider-logo">
```

### Sonstige Bilder (`images/misc/`)
Alle anderen Bilder. Benennung: `{name}.{ext}`

**Beispiel:**
- `a-10-warthog.png`
- `background.jpg` - **WICHTIG: Hintergrundbild der Website**

**In `index.html` verwenden:**
```html
<img src="images/misc/a-10-warthog.png" alt="A-10 Warthog" class="airplane">
```

**Hintergrundbild:**
Das Hintergrundbild wird automatisch in `style.css` geladen:
```css
background-image: url('images/misc/background.jpg');
```
**Hinweis:** Das Bild sollte `background.jpg` oder `background.png` heißen und im `images/misc/` Ordner liegen.

## Migration von Discord-Links

1. Lade die Bilder von den Discord-Links herunter
2. Benenne sie entsprechend der oben genannten Konventionen
3. Speichere sie in den entsprechenden Ordnern
4. Aktualisiere die Pfade in:
   - `data/operations.json`
   - `data/availability.json`
   - `index.html`

## Unterstützte Bildformate

- `.jpg` / `.jpeg`
- `.png`
- `.gif`
- `.webp`
- `.svg`


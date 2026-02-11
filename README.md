# 🖐 Gestuelle Interactive – Travaux Dirigés

## Structure des fichiers à respecter

```
projet/
├── index.html
├── TD1/
│   ├── config.json
│   ├── 1.png … 7.png
├── TD2/ … TD10/
│   └── (même structure)
```

## Format config.json (dans chaque dossier TDx/)

```json
{
  "td": "TD1",
  "images": [
    {
      "id": 1,
      "file": "1.png",
      "zones": [
        { "pt1":{"x":80,"y":60}, "pt2":{"x":220,"y":140}, "targetImage":"2.png", "label":"Zone 1" },
        { "pt1":{"x":260,"y":60}, "pt2":{"x":400,"y":140}, "targetImage":"3.png", "label":"Zone 2" },
        { "pt1":{"x":80,"y":180}, "pt2":{"x":220,"y":260}, "targetImage":"4.png", "label":"Zone 3" },
        { "pt1":{"x":260,"y":180}, "pt2":{"x":400,"y":260}, "targetImage":"5.png", "label":"Zone 4" },
        { "pt1":{"x":80,"y":300}, "pt2":{"x":220,"y":380}, "targetImage":"6.png", "label":"Zone 5" },
        { "pt1":{"x":260,"y":300}, "pt2":{"x":400,"y":380}, "targetImage":"7.png", "label":"Zone 6" }
      ]
    }
  ]
}
```

## Gestes
- Index levé main droite → sélection de zone
- Pinch 2 mains + écarter/rapprocher → zoom 1×–8×
- Pinch 2 mains + déplacer → translation
- Bouton Déconnexion → export JSON + retour login

## Journal exporté
Fichier: Actions-TD1-Dupont-Marie.json (téléchargement auto à la déconnexion)
Types d'actions: connexion, chargement_image, selection_zone, zoom_debut, zoom_fin, deconnexion

## Lancer en local (obligatoire pour fetch JSON)
```bash
python -m http.server 8080
# ou: npx serve .
```

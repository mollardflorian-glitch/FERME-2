# Terres & Troupeau — PWA locale

Application 100 % hors ligne, sans serveur applicatif ni dépendance externe. Les données sont conservées dans le `localStorage` du navigateur.

## Android + GitHub Pages
1. Créer un dépôt **privé** (recommandé) et y déposer le contenu du dossier décompressé.
2. Dans Settings → Pages, choisir la branche et le dossier `/root`.
3. Ouvrir l’URL Pages sur Android, puis menu Chrome → **Ajouter à l’écran d’accueil**.
4. Faire une première sauvegarde via Réglages → JSON. Tester l’import sur un autre appareil avant toute suppression.

> Confidentialité : ne publiez jamais un dépôt public contenant le fichier `data-seed.json` si les parcelles ou informations de l’exploitation sont considérées comme personnelles. Préférez le zip « vide » et importez `donnees-ferme.json` localement.

## Ordinateur / serveur local
Double-cliquer `index.html` fonctionne pour la saisie et les exports. Pour activer le service worker hors ligne et tester comme GitHub Pages : `python3 -m http.server 8000`, puis ouvrir `http://localhost:8000`.

## Données initiales et sauvegardes
- `data-seed.json` contient les parcelles PAC, cultures 2026, historique d’assolement et le catalogue d’effluents à teneurs **0 / à valider**.
- Réglages permet export JSON complet, CSV interventions/apports et .xls simple.
- Le bouton Réinitialiser revient aux données préchargées et demande confirmation.
- Le calcul fumure est `dose × teneur × surface`; aucune norme d’effluent n’est inventée.

## Périmètre
Les teneurs des effluents, les besoins par culture et les estimations d’effluents d’élevage doivent être saisis/validés par l’utilisateur.

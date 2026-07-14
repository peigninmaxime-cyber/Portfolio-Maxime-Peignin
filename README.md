# Portfolio — Maxime Peignin

Site statique reproduisant l'effet "livre qu'on feuillette" (comme Flipsnack), avec 3 vidéos intégrées (pages 7, 17, 18). Gratuit à héberger, aucune dépendance de service payant.

## Structure
```
index.html          → tout le site (HTML + CSS + JS)
pages/page-01.jpg … page-20.jpg   → les pages du portfolio (converties depuis le PDF)
vendor/page-flip.browser.js       → librairie open source pour l'effet page-flip (embarquée en local, pas de CDN)
```

## Déployer gratuitement sur GitHub Pages

1. Crée un nouveau repo sur GitHub (ex. `portfolio`), public.
2. Mets tous les fichiers de ce dossier (`index.html`, `pages/`, `vendor/`) à la racine du repo.
3. Sur GitHub : Settings → Pages → Source → Branch `main`, dossier `/ (root)` → Save.
4. Après ~1 minute, ton site est en ligne à :
   `https://TON_PSEUDO.github.io/portfolio/`

## Modifier plus tard

- **Changer une page** : remplace le fichier `pages/page-XX.jpg` correspondant (garde le même nom).
- **Ajouter/retirer une vidéo** : dans `index.html`, cherche la constante `VIDEO_PAGES` en bas du fichier et ajoute/enlève une entrée `numéro_de_page: { id: "IDENTIFIANT_YOUTUBE", vertical: true/false }`.
  `vertical: true` pour un format Short/vertical, `false` pour un format YouTube classique 16:9.
- **Nombre total de pages** : mets à jour la constante `TOTAL_PAGES`.

## Notes techniques

- Les 3 vidéos ne sont pas incrustées directement "dans" la page qui tourne (techniquement compliqué et instable pendant l'animation), mais s'ouvrent en plein écran au clic sur la miniature — comportement standard et fluide sur desktop et mobile.
- Le site est 100% statique : aucun serveur, aucune base de données, aucun coût d'hébergement.

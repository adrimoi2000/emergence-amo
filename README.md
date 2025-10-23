# Emergence AMO – Landing Page

Site vitrine statique pour Emergence AMO, cabinet d’accompagnement à la maîtrise d’ouvrage spécialisé en bâtiment durable, éco-conception et économie circulaire.

## Structure du projet
- `index.html` — page unique avec TailwindCSS livré via CDN.
- `styles.css` — compléments CSS pour les cartes, formulaires et effets d’hover.
- `assets/` — favicon et visuels fictifs (SVG). Remplacez-les par vos images optimisées.
- `AGENTS.md` — guide de contribution pour l’équipe technique.

## Modifier le contenu
1. Ouvrez `index.html` dans votre éditeur.
2. Les sections sont balisées (`id="missions"`, `id="methode"`, etc.) : remplacez textes, titres et témoignages directement dans le HTML.
3. Pour changer la palette ou la typographie, ajustez le script Tailwind dans `<head>` (objets `colors` et `fontFamily`) et complétez si besoin `styles.css`.
4. Mettez à jour les SVG de `assets/` avec vos visuels (préférez 1200×630 pour `og-image.svg`) afin d’améliorer l’aperçu social.

## Prévisualisation locale
Servez simplement le dossier courant avec Python :
```bash
python3 -m http.server 5173
```
Puis ouvrez `http://127.0.0.1:5173` dans votre navigateur.

## Déploiement
### GitHub Pages
1. Poussez le dépôt sur GitHub (`main` ou `gh-pages`).
2. Dans *Settings → Pages*, sélectionnez la branche et le dossier `/ (root)`.
3. Attendez la génération (quelques minutes) puis vérifiez l’URL fournie.

### Netlify
1. Créez un site via le bouton “Add new site → Deploy manually”.
2. Glissez-déposez le dossier du projet ou connectez le dépôt Git.
3. Aucune commande de build n’est requise (site statique pur).
4. Configurez le domaine personnalisé depuis l’onglet “Domain management”.

## Formulaire de contact
Le formulaire actuel déclenche votre messagerie via `mailto:contact@emergence-amo.fr`. Pour un envoi côté serveur :
- **Formspree** : changez l’attribut `action` par l’URL fournie et ajoutez un champ caché `_subject`.
- **Netlify Forms** : ajoutez `data-netlify="true"` au `<form>` et créez un champ caché `name="form-name"` pour la collecte.

## Accessibilité & SEO
- Contraste AA assuré par la palette vert profond / gris ciment.
- Métadonnées (`title`, `meta description`, Open Graph) déjà définies : adaptez-les à vos campagnes et domaines.
- Vérifiez la validité HTML5 via [validator.w3.org](https://validator.w3.org/) après chaque mise à jour.

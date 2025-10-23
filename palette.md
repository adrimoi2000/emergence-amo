# Palette & Typographie

## Couleurs
- **Vert primaire — `#0E6B3C`**  
  Utilisé pour les aplats principaux (hero, boutons, icônes). Toujours sur texte blanc pour garantir le contraste AA.
- **Vert profond — `#0B5A31`**  
  Variante assombrie pour les états hover, focus et les dégradés. À réserver aux survols et aux fonds secondaires.
- **Vert accent — `#34D399`**  
  Teinte lumineuse pour les éléments graphiques (icônes SVG, soulignements) et les données chiffrées.
- **Gris fond — `#F3F4F6`**  
  Couleur d’arrière-plan globale et des champs de formulaire. Assure une base douce et lumineuse.
- **Gris texte — `#111827`**  
  Couleur par défaut pour les titres et paragraphes. Jouer avec les opacités Tailwind (`/60`, `/80`) pour les nuances.
- **Blanc — `#FFFFFF`**  
  Fond des cartes, blocs témoignages et formulaires. Conserver des ombres douces pour détacher du fond.

## Typographie
- **Police principale : `Inter`** (via Google Fonts).  
  Poids utilisés : 400, 500, 600, 700. Lecture confortable sur desktop comme mobile.
- **Fallback système :** `system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif`.  
  Vérifiez que les interfaces restent harmonieuses si Google Fonts ne se charge pas.

## Bonnes pratiques
- Maintenir un contraste minimum de 4.5:1 pour les textes.  
- Appliquer les rayons de bordure existants (24 px) pour conserver l’identité douce de la page.  
- Pour les données chiffrées ou highlights, combiner `#0E6B3C` (texte) et `#34D399` (fond translucide).

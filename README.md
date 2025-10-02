# For-fun.io

### Description

Intégration statique en HTML/CSS d’un site vitrine pour un collectif de développeurs (workshops, talks, mini-formations). L’objectif est la fidélité visuelle de la maquette sans logique JavaScript ni backend.

### Maquette

Lien Figma d’origine: `https://www.figma.com/design/LIuuSL8mPBJIR01BoPtrYi/Untitled?node-id=63-212`

## Démarrage rapide

- Télécharger/cloner le dépôt
- Ouvrir `index.html` dans un navigateur moderne
- Aucun build, serveur ou dépendance n’est requis

## Technologies

- HTML5
- CSS3

## Structure du projet

- `index.html` — structure HTML et contenu
- `style.css` — styles globaux et de sections
- `Assets/imgs/` — images des intervenants

## Conventions de nommage

Les classes ont été nommées pour gagner en clarté :

- Hero: `hero`, `hero__intro`
- Speakers: `speakers`, `speakers__grid`, `speaker-card-1`, `speaker-card-2`, `speaker-card-3`
- Bloc deux colonnes: `split-panels`, `split-panels__left`, `split-panels__right`
- Planning: `schedule` (titre), `schedule__header`, `schedule__divider`, `schedule__row-1` … `schedule__row-5`

## Variables CSS

Définies dans `:root` (couleurs principales du thème) :

- `--color1` (primaire)
- `--color2` (blanc)
- `--color3` (gris texte)
- `--color4` (noir)
- `--color5` (primaire-hover)

## Sections et comportements visuels

- Navigation: barre fixe en haut avec palette primaire
- Hero: titre + description centrés
- Speakers: grille de 3 intervenants (photo, nom, bio courte)
- Split panels: 2 colonnes 50/50 avec titres et paragraphes
- Schedule (planning):
  - `schedule__header` définit les intitulés de colonnes
  - `schedule__row-n` affiche 3 colonnes: sujet, date/heure, salle
  - Le premier paragraphe de chaque ligne (intitulé) est aligné à gauche; le reste est centré
  - Le bouton “Voir plus” clôt la section

## Accessibilité et contenu

- Renseigner des attributs `alt` descriptifs pour les images (`Assets/imgs/*`).
- Conserver une hiérarchie sémantique des titres (h1, h2, h3...).
- Le planning pourrait être présenté en tableau sémantique si nécessaire (choix maquette ici: grid).

## Maintenance courante

- Ajouter un intervenant: dupliquer un bloc `speaker-card-X` dans `speakers__grid` et adapter l’image, le nom et la bio.
- Ajouter une session: dupliquer la dernière `schedule__row-N` (incrémenter N) et mettre à jour intitulé, date/heure, salle.
- Modifier les couleurs: ajuster les variables dans `:root` de `style.css`.

## Compatibilité et limites

- Ciblé desktop (non responsive volontairement).
- Compatibilité: Chrome/Edge/Firefox récents.

## Feuille de route (suggestions)

- Ajout d’une version responsive (breakpoints 1024/768/480)
- Factoring CSS des lignes du planning pour réduire la duplication
- Optimisation des images (dimensions + compression)

## Licence

Usage libre à des fins personnelles et pédagogiques.

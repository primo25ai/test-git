# Portfolio — Designer & Développeur

Landing page portfolio en HTML/CSS/JS vanilla, sans dépendances ni framework.

## Aperçu

Site vitrine one-page pour un designer/développeur : hero avec mark géométrique animé, section projets, compétences et contact.

## Design

- **Palette** — neutres chauds (encre `#1C1C1E`, pierre `#EDEAE5`, papier `#FAFAF8`) avec un accent unique rouge oxyde `#B44536`
- **Typographie** — [Syne](https://fonts.google.com/specimen/Syne) (titres, display) + [Inter](https://fonts.google.com/specimen/Inter) (texte courant), chargées via Google Fonts
- **Signature visuelle** — mark géométrique SVG (cercle, croix, triangle) qui se dessine au chargement du hero
- **Photos** — images libres de droit (Unsplash) illustrant chaque projet, arrière-plan du hero
- **Animations** — révélation au scroll (IntersectionObserver), micro-interactions au survol, `prefers-reduced-motion` respecté

## Structure

```
index.html          Structure de la page (hero, projets, compétences, contact)
style.css           Palette, typographie, layout, animations, responsive
images/hero-bg.jpg   Image d'arrière-plan du hero
images/img-*.jpg     Illustrations des cartes projets
```

## Sections

- **Accueil** — hero plein écran avec mark animé et CTA
- **Projets** — grille de 3 cartes avec photo, titre et description
- **Compétences** — grille de 4 compétences avec icônes SVG
- **Contact** — liens sociaux et informations de contact

## Responsive

- Breakpoints à 768px et 480px
- Menu hamburger sous 768px (panneau latéral avec overlay)
- Typographie fluide (`clamp()`), grilles en colonne unique sur mobile

## Lancer le projet en local

Aucune installation requise — fichiers statiques servis par n'importe quel serveur HTTP :

```sh
python -m http.server 8080
```

Puis ouvrir [http://localhost:8080](http://localhost:8080).

Une configuration `.claude/launch.json` est fournie pour lancer le serveur automatiquement depuis Claude Code.

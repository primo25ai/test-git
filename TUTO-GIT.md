# Tuto Git — Mémo pour ce projet

Petit guide des commandes Git utilisées pour initialiser et faire vivre ce dépôt, à garder sous la main.

## 1. Initialiser le dépôt et le relier à GitHub

```sh
git init
git remote add origin https://github.com/primo25ai/test-git.git
```

- `git init` — crée un dépôt Git local dans le dossier courant
- `git remote add origin <url>` — associe le dépôt local au dépôt distant sur GitHub, sous l'alias `origin`

## 2. Premier commit et envoi

```sh
git status                       # affiche l'état des fichiers (modifiés, non suivis...)
git add index.html                # met le fichier en attente de commit ("staging")
git commit -m "First Commit"      # enregistre un instantané avec un message
git push --set-upstream origin master   # envoie vers GitHub et lie la branche locale à origin/master
```

Une fois le lien établi avec `--set-upstream`, un simple `git push` suffit pour les envois suivants.

## 3. Cycle de travail habituel

À répéter à chaque modification :

```sh
git status          # voir ce qui a changé
git diff             # voir le détail des modifications non indexées
git add <fichier>    # ou "git add ." pour tout ajouter
git commit -m "message clair décrivant le changement"
git push
```

## 4. Exemple de sortie réelle d'un `git push`

```
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 424 bytes | 141.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/primo25ai/test-git.git
   973d59b..e9e47e8  master -> master
```

Le hash affiché (`973d59b..e9e47e8`) montre le déplacement de la branche locale vers son nouvel état sur GitHub.

## Aide-mémoire des commandes courantes

| Commande | Rôle |
|---|---|
| `git status` | État des fichiers (suivis, modifiés, indexés) |
| `git add <fichier>` | Indexer un fichier pour le prochain commit |
| `git add .` | Indexer tous les fichiers modifiés/nouveaux |
| `git commit -m "message"` | Créer un commit avec les fichiers indexés |
| `git push` | Envoyer les commits locaux vers GitHub |
| `git pull` | Récupérer et fusionner les changements distants |
| `git diff` | Voir les changements non indexés |
| `git log --oneline` | Historique condensé des commits |
| `git branch` | Lister les branches locales |
| `git checkout -b <nom>` | Créer et basculer sur une nouvelle branche |

## Bonnes pratiques

- Écrire des messages de commit clairs, au présent, décrivant le **pourquoi** plutôt que le **quoi**
- Faire des commits petits et fréquents plutôt qu'un gros commit fourre-tout
- Toujours `git status` avant un `add`/`commit` pour vérifier ce qui part réellement
- Éviter de commiter des fichiers sensibles (clés API, `.env`, identifiants)

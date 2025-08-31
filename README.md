# DOCUMENTATION &#9989;
Date: 30/08/2025 à 16h

## Projet: Création du répertoire: test-git

## Sur Terminal de VSC !
GitHub_Primo\test-git>:
```sh
git init
git remote add origin https://github.com/primo25ai/test-git.git
git status
git add index.html
git status
git commit -m "First Commit"
git push
git push --set-upstream origin master
git diff /Montre les modifications de fichier qui ne sont pas encore indexées
git add index.html
git status
git commit -m "2nd Commit"
git status
````
```sh
git push [alias] [branche] /Envoie tous les commits de la branche locale vers GitHub
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 424 bytes | 141.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/primo25ai/test-git.git
   973d59b..e9e47e8  master -> master
````

Mise à jour réussi (local @ github) !!!

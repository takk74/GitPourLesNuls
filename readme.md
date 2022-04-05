---
title: Git Cheat Sheet Collaborative
tags: courses, B3 BWSM, cheat sheet, git
---

![](https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vue.js&logoColor=4FC08D)
[![Fabriqué en - France](https://img.shields.io/badge/Fabriqué_en-France_🇫🇷-1A90FF)](https://portfolio.corentinperroux.fr)
## Git c'est quoi ?

### Centralisé vs Décentralisé (SVN vs GIT)

Contrairement à Git, SVN est un système de contrôle de version centralisé. Cela signifie que sur Git, chaque participant a un clone de l'ensemble du référentiel alors que SVN fonctionne avec référentiel central. 
![](https://i.imgur.com/1y5hsmC.jpg)


### Les 5 niveaux de Git

![](https://i.imgur.com/00plXRF.png)

* La remise `stash`: **C'est un endroit où on va pouvoir stocker des modifications (les figer dans le temps), pendant que l'on change de branche par exemple. Une fois qu'on en a besoin, on peut les récupérer comme si rien ne s'était passé.**
* L’Espace de travail workspace: **Notre flux de travail, c'est là où on travail, notre base de code.**
* L’Index index: **C'est la "zone de staging", c'est là où on enregistre les changements avant de les commit. C'est une sorte de pré-enregistrement pour choisir ce que l'on va commit.**
* Le dépot Local Local Repository: **C'est l'endroit où l'on va stocker les changement après avoir commit. C'est le stockage des commit et c'est ici que se créé l'historique. C'est là que sont stocké tous nos changement et toutes nos branches au fur et à mesure de l'avancée du projet.**
* Le dépot Distant Remote Repository: **C'est la même chose que le repository local (dépot local) mais sur un serveur exterieur (Github, Gitlab, Bitbucket,...). On peut envoyer nos modifications locales (sur le dépot local) sur le dépot distant afin de les stocker ailleurs et pouvoir les récupérer n'importe où et n'importe quand dans le monde. C'est également grace à ça qu'on va pouvoir partager du code, récupérer du code et collaborer avec d'autres développeurs sur des projets open-source.**


## Quelques commandes

### `git init`
> Initialiser un dépot GIT.

### `git add FILE...`
> Ajouter des fichiers modifiés dans la "zone de staging" (l'"index").

### `git commit -m 'SOME MESSAGE'`

> Créer un commit pour effectuer une "sauvegarde".

### `git stash`
> Stocker des données non "sauvegardées" afin de faire autre chose pendant un temps donné sans se soucier de ces modifications (changer de branche par exemple).

### `git stash pop`
> Permet de réappliquer les modifications contenues dans un "stash" puis de supprimer le "stash".

### `git clone URL`
> Cloner un dépot distant sur sa propre machine et ainsi créer un dépot local du dépot distant en question.

### `git push`
> Envoyer l'état du dépot local sur le dépot distant.

### `git pull` 
> Récupérer l'état du dépot distant sur le dépot local.

## Branches
Git fonctionne avec un système de branches qui permet de cloisonner l’avancée de chacun.

### `git branch NEW_BRANCH` 
> Cette commande permet de créer une nouvelle branche. Dans ce cas précis, la branche s'appellera "NEW_BRANCH".

### `git checkout NEW_BRANCH`
> Cette commande permet de changer de branche. Dans ce cas précis, on se déplace sur la branche "NEW_BRANCHE".

#### Argument `-b`
> Spécifier -b provoque la création d’une nouvelle branche.

### `git merge NEW_BRANCH`
> Cette commande permet de fusionner le code de la branche "NEW_BRANCHE" sur la branche actuelle. 

### `git rebase OLD_BRANCH`
> Permet de transférer notre branche sur une autre. Et sera donc considérer comme la suite de celle-ci.
> Applique l'historique d'une branche sur une autre branche.

### `git branch -D SOME_BRANCH`
> Cette commande permet de supprimer une branche même s'il reste du contenu non sauvegardé dessus.

## Tagging

### `git tag -a 1.4 -m 'ma version 1.4'`
> Crée le tag 1.4 et lui donne la message "ma version 1.4"

### Lister tout les tags
> git tag
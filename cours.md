# Git

## Introduction

Git est un logiciel qui vous permet de suivre les modifications apportées à un projet au fil du temps. Git fonctionne en enregistrant les modifications que vous apportez à un projet, en stockant ces modifications, puis en vous permettant d'y faire référence au besoin.

## git init

Le mot "init" signifie `initialiser`. Cette commande configure tous les outils nécessaires à Git pour commencer à suivre les modifications apportées au projet.

## Flux de travail Git

Un projet Git peut être envisagé comme ayant trois parties :

- **Répertoire de Travail** : où vous effectuerez tout le travail : créer, éditer, supprimer et organiser des fichiers.
- **Zone de Staging** : où vous listerez les modifications apportées au répertoire de travail.
- **Dépôt** : où Git stocke définitivement ces modifications sous forme de différentes versions du projet.

Le flux de travail Git consiste à éditer des fichiers dans le répertoire de travail, ajouter des fichiers à la zone de staging, et sauvegarder les modifications dans un dépôt Git. En Git, nous sauvegardons les modifications avec un commit, sujet que nous approfondirons dans cette leçon.

## git status


Pour vérifier l'état des modifications dans le répertoire de travail, vous pouvez utiliser la commande suivante 

```bash
git status
```

Cette commande vous fournira des informations sur les fichiers modifiés, ajoutés à la staging area, ou prêts à être commités dans le dépôt Git.

## git add
Pour que Git commence à suivre les changements dans un fichier, celui-ci doit être ajouté à la "zone de staging" ou "zone d'index" ou "staging area". On utilise la commande:
```bash
git add nom_du_fichier
```
Les fichiers ainsi mis dans la staging area, sont donc prêts pour la prochaine sauvegarde

## git diff

Nous pouvons vérifier les différences entre le répertoire de travail et la zone de staging avec la commande:
```bash
git diff nom_du_fichier
```

## git commit

Un `commit` est la dernière étape de notre flux de travail avec Git. Un commit enregistre de manière permanente les modifications de la zone de staging dans le dépôt.
`git commit` est la commande que nous allons exécuter ensuite. Cependant, pour effectuer un commit, une autre partie de code est nécessaire: l'option `-m` suivie d'un message. Voici un exemple:
```bash
git commit -m "Mon message"
```

### Conventions standards pour les messages de commit:
- Doivent être entre guillemets
- Ecrits au présent
- Devraient être brefs (50 caractères maximum)

## git log

Souvent avec Git, vous aurez besoin de vous référer à une version antérieure d'un projet. Les commits sont stockés chronologiquement dans le dépôt et peuvent être visualisés avec la commande:
```bash
git log
```
Dans la sortie du terminal, vous verrez affiché:
- Un code 40 caractères, appelé SHA, qui identifie de manière unique le commit. 
- L'auteur du commit et son adresse mail
- La date et l'heure du commit
- Le message de commit.

## Résumé

Pour résumer:
* Git est le système de contrôle de version standard de l'industrie pour les développeurs web.
* On utilise des commandes Git pour suivre les modifications apportées à un projet:
- `git init` crée un nouveau dépôt git
- `git status`inspecte le contenu du répertoire de travail et de la zone de staging
- `git add` ajoute des fichiers du répertoire de travail à la zone de staging
- `git diff` montre la différence entre le répertoire de travail et la zone de staging
- `git commit` enregistre de manière permanente les modifications de fichiers de la zone de staging dans le dépot
- `git log` affiche une liste de tous les commits précédents
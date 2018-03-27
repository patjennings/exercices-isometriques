## Écrire l'article

#### Ajouter une image


## Nom du fichier
Le fichier doit être nommé de la façon suivante : `Y-m-d-the-title.md`
Le nom du fichier n'est important qu'à titre de repère : c'est le champ `titre` des métadonnées de l'article qui s'affichera en tête de l'article

## Métadonnées

```
---
layout: post
title:  "Le titre de l'article"
date:   2018-03-27 13:43:00 +0100
categories: article
---

Et là, on écrit le contenu

## Des titres
Re-du texte.

Une image ? Ok…
![Là, le titre de l'image](http://www.esacademic.com/pictures/eswiki/70/Frutiger_mostra1.jpg)

```

## Publier un article
```bash
$ git pull
```
```bash
$ git commit -m
```
```bash
$ git push -u origin master
```

Comment publier un article sur Les Exercices Isométriques.
## Écrire l'article

Le texte, c'est du markdown. Rien de compliqué. [Là, on a un référentiel](https://guides.github.com/features/mastering-markdown/) des options de formatage, si on veut enrichir un peu.

Je pars du principe qu'on écrit son article sur sa machine, et qu'on uploade le fichier `.markdown`/`.md` ensuite.

### Ajouter une image
Soit on appelle une image des internets, soit on la pose sur le git au préalable.
Pour poser une image sur le git, rien de plus simple :
0. On va sur le repository, sur la branche `gh-pages`… Ou on y va en [cliquant là-dessus](https://github.com/patjennings/exercices-isometriques/tree/gh-pages)
0. Là, on va dans [`images/`](https://github.com/patjennings/exercices-isometriques/tree/gh-pages/images)
0. Et on uploade l'image ― en haut à droite, bouton `Upload files`
0. Une fois que c'est bon, on récupère l'url de l'image ― e.g. clic droit > Copier l'adresse de l'image

Et là, on peut ajouter l'image dans notre contenu en markdown, en collant l'url entre les parenthèses :
```
![Titre de l'image ― optionnel](https://github.com/patjennings/exercices-isometriques/blob/gh-pages/images/vue-1916_sv-verdun.png.png?raw=true)
```
> Ne pas oublier le point d'exclamation, devant les crochets, sinon c'est juste un lien, l'image ne s'affiche pas

### Ajouter des vidéos externes, Vimeo, Youtube

On peut coller directement le code d'intégration HTML fourni par le provider, dans le corps de l'article. Exemple avec Youtube :
```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/x537Cqg5nEI" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
```

## Nom du fichier

Le fichier doit être nommé de la façon suivante : `Y-m-d-the-title.md`
Le nom du fichier n'est important qu'à titre de repère : c'est le champ `titre` des métadonnées de l'article qui s'affichera partout.

## Métadonnées

Une fois l'article écrit, on va venir coller ça en tête du fichier (bien prendre les lignes de tirets au dessus et en dessous du bloc) ― c'est ce qui permet au moteur de transformer notre markdown en page web :
```
---
layout: post
title:  "Le premier article du blog"
date:   2018-03-27 00:00:00 +0100
categories: article
author: Thomas
excerpt_separator: <!--more-->
---
```

Explications. En gras, les trucs les plus importants pour publier
- `layout` : le template HTML que Jekyll appelle pour afficher la page.
- **`title` : le titre du billet qui s'affiche partout**
- **`date` : la date de publication de l'article, à remplir à la mano selon le même format. L'heure, on s'en fout un peu, de toutes façons elle ne s'affiche pas.**
- `categories` : ça, on s'en fout, c'est pour faire des regroupements, des trucs comme ça. Il vaut mieux ne pas changer ça, car ça apparait dans l'url
- **`author` : le nom de l'auteur, hé ! Matthieu ou Thomas, quoi…**
- **`excerpt_separator` : en collant le `<!--more-->` où tu veux dans ton texte, tu peux choisir, sur la liste des posts de l'accueil, où l'extrait qui apparait sous le titre sera coupé. Si tu ne le mets nulle part, ça affiche tout l'article, ce qui n'est pas top niveau rendu.** On verra si on garde ça, je ne sais pas trop…

## Publication

Une fois que tout ça est fait, on se rend sur le repository ([`patjennings/exercices-isometriques`](https://github.com/patjennings/exercices-isometriques/tree/gh-pages)), **sur la branche `gh-pages`**:
- On va dans le dossier`_posts/`
- On clique sur `Upload files`, en haut à droite
- On uploade, et c'est bon !

> La branche gh-pages, c'est celle qui permet de transformer nos tas de fichiers en un site HTML propre, avec une url et tout. Elle est automatisé pour servir en façade des fichiers HTML, comme un serveur Apache. L'autre, la branche master, créée par défaut, permet uniquement, comme n'importe quelle autre branche, de stocker des fichiers

## Résultat

Le résultat devrait être visible ici, quelques minutes plus tard :
> [https://patjennings.github.io/exercices-isometriques/](https://patjennings.github.io/exercices-isometriques/)

## Troubleshooting

- Si le post n'apparait pas tout de suite, c'est normal. Il faut quelques minutes à github pour générer la page
- Si au bout d'un quart d'heure, il n'apparait toujours pas, checker qu'on a bien publié notre article dans le dossier `_posts/` et, surtout, sur la branche `gh-pages`.
  - Pour changer de branche, si on est sur la branche `master` e.g., il faut aller à la racine du repository ([`patjennings/exercices-isometriques`](https://github.com/patjennings/exercices-isometriques/))
  - Puis, cliquer sur le select en haut à gauche, `Branch: master`, et basculer sur `gh-pages`.

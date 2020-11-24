# Taxonomie de contenu et administration avec Forestry

Dans ce chapitre, nous verrons ce que sont les typologies de contenus, leur taxonomies et comment les administrer avec [Forestry](https://forestry.io).

## Typologie de contenu

Pour déterminer ma stratégie de communication en ligne, il me faut maîtriser la **typologie des informations** que je souhaite proposer. En d’autres mots, je dois pouvoir identifier et distinguer les types d’information que je peux donner à mes publics et adapter ces types à leurs **besoins**, **comportements** et **tendances**.

Voici quelques exemples de types de contenu et leur usage :

### Les pages

Elles sont dites de type "hiérarchique. C'est à dire qu'elles peuvent s'organiser en arborescence. En d'autres termes, une page peut être enfant de sa parente.

Exemple :

```
- Présentation
  - Notre histoire
  - Nos valeurs
  - ...
- L'école
  - Le programme pédagogique
  - L'équipe d'enseignants
  - ...
```

### Les articles

Dites non hiérarchique. C'est à dire que chaque article est au même niveau que les autres :

En revanche, contrairement aux pages, ils sont classés par date de publication. Puis qu'ici, ce qui est important, c'est de placer son article d'actualité dans une temporalité. C'est ainsi que la plus part des médias (ex. *Le Monde*, *Le Parisien*, *Paris-Normandie*, etc...) fonctionne. De ce fait, la date est une information que l'on doit pouvoir exploiter.

On peut donc retrouver cette information dans le nom du fichier :

```
- 2020-11-24-mon-second-article.md
- 2020-11-22-mon-premier-article.md
- ...
```

Le classement systeme des fichiers par rapport à leur nom fait naturellement le classement.

On peut aussi décider d'exploiter cette information comme une data que nous retrouverons, dans notre exemple en Markdown, dans le frontmatter

```
---
title: "Mon titre d'aticle"
date: 2020-11-24
---
```


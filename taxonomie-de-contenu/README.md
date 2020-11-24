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

Et les informations dont nous aurions besoin pour notre page seraient "Le titre" et "Le contenu". Ce qui pourrait se traduire en markdown par :

```
---
title: "Titre de ma page"
---

# Titre de ma page

Ici le contenu de ma page au format Markdown
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

On peut aussi décider d'exploiter cette information comme une data que nous retrouverons, dans notre exemple en Markdown, dans le frontmatter. Et ici, contrairement aux pages, nous aurions besoin du nom de l'auteur que nous ajouterons dans notre Frontmatter :

```
---
title: "Mon titre d'aticle"
date: 2020-11-24
author: "Raphael"
---

# Titre de mon article

Contenu de l'article au format markdown...
```

## Taxonomies

Les taxonomies permettent de classer nos contenus en catégories. On peu aussi créer plusieurs taxonomies différentes. Dans notre exemple ci-dessous, nous retrouvons deux taxnomies. "Catégories" et "tags"

```
---
title: "Mon titre d'aticle"
date: 2020-11-24
author: "Raphael"

categories: ["Cours"]
tags: ["Taxonomies", "Rédactionnel", "Web"]
---

# Titre de mon article

Contenu de l'article au format markdown...
```

## Les metas

Les metas permettent d'ajouter des informations à un contenu.

Dans le cas par exemple d'une fiche de film, nous aurions besoin de : l'année de sortie, le réalisateur, etc...

Nous pourrions le traduire ainsi dans notre frontmatter :

```
---
title: "La Ligne verte"
date: 2020-11-24

genres: ["Policier", "Fantastique"]

realisateur: "Frank Darabont"
sortie: "1 mars 2000"
duree: "3h09min"
---

# La Ligne verte

Paul Edgecomb, Gardien-chef du pénitencier de Cold Mountain en 1935, était chargé de veiller au bon déroulement des exécutions capitales. Parmi les prisonniers se trouvait un colosse du nom de John Coffey...
```

Vous constaterez également que nous avons ajouté une nouvelle taxonomie "Genre" qui nous permettra de regrouper les films par genre.

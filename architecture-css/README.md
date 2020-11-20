# Architecture CSS et approche modulaire

Assurer une bonne maintenance et scalabilité de son design passe par une bonne organisation de la base de code. Le CSS est particulièrement concerné et cela peut vite devenir compliqué de maintenir son interface sans régressions.

## Architecture, structurez votre code

### ITCSS Un exemple d'architecture CSS

ITCSS Une architecture imaginée par [Harry Roberts](https://csswizardry.com/). ITCSS organise l’ordre d’inclusion des feuilles de styles. ITCSS = Inverted Triangle CSS. L’inclusion des règles de styles est réalisée par spécificités :

  - moins forte -> plus forte
  - générique -> explicite

Cela à plusieurs avantages, le premier étant la séparation des styles de structure et des styles de forme avec la pratique de l’Oriented Object CSS (OOCSS). Second avantage, maitrise de la cascade CSS avec minimisation des surcharges. On peut parler de surcharge maitrisée grâce à un ordre d’inclusion des styles bien spécifique :

  - Settings
  - Tools
  - Generic
  - Elements
  - Objects
  - Components
  - Utilities

**Settings & Tools** :
Avec des pré-processeurs comme "Sass" ou "postcss" il est possible de profiter de variables, fonctions et mixins qui forment notre boite à outils. Ces éléments servent à la compilation du code en CSS.

**Generic** :
Dossier où se retrouvent les styles de cohérence cross-browser. On y inclu les normalize.css et autre reset permettant d'annuler les styles par défaut des navigateurs. On y met également les styles partagés sur tous où un groupe d'éléments HTML, comme le box-sizing par exemple.

**Élements** :
On retrouve ici les styles spécifiques à certains de nos éléments HTML. Les styles titres, images, ou encore à l'élément HTML par exemple.

**Objects** :
Styles concernant nos objets CSS. Les objets CSS représentent des styles de structure pouvant être utilisés sur tous nos éléments/composants. Dépourvus d'esthétique, ils servent à gérer le positionnement/comportement de nos élements. Par exemple un objet wrapper utilisé pour piloter le comportement d'une boite dans laquelle nous viendrions mettre du contenu (paddings, max-width…).

**Components** :
Styles spécifiques à nos composants UI. La plupart de notre design et de notre travail se trouvera ici. Exemple : un composant button avec son UI bien spécifique.

**Utilities** :
Classes utilitaires de styles spécifique. Ce sont de véritable Helpers qui nous permettent d'appliquer des styles sur des éléments autre que des composants et de surcharger n'importe quel style existant. Pratique pour compléter les objets.

C'est une proposition pas une obligation. On peu très bien l'adapter à ses besoins. Voici un exemple d'organisation que j'utilise et qui respecte le même principe :

```
- Settings : déclaration de variables
- Base : styles génériques
- Layout : structure de la page
- Composants : un fichier par composant
  - heading
  - boutons
  - menu
  - ...
- Thème : styles spécifiques à un theme ou une page
- Helpers : ensemble de classe utilitaire
```

## Conventions d'écritures, apportez de la clarté dans votre code

Les conventions de nommage sont très importantes pour collaborer à plusieurs sur de gros projets. Plusieurs impacts :

  - Logique commune
  - Scope : éviter les surcharges indésirables et se faire surprendre par la cascade CSS
  - Lisibilité du code

Les CSS modules et POST-CSS permettent de facilement contrer le deuxième point de cette liste. Cependant pour la lisibilité du code il reste important de garder une convention commune entre développeurs.

### BEM, un exemple de convention d'écriture populaire

BEM est une convention de nommage afin de fournir une logique et une rigueur au noms des classes CSS. BEM -> Block Element Modifier, sous la forme de .block__element--modifier :

  - `.avatar` représente le block
  - `.avatar__img` représente un élément du block
  - `.avatar__img--rounded` représente un modifier de l'élément


## Mettre en forme son code

Normaliser l'écriture de son CSS (et de son HTML) pour un code cohérent, flexible et durable

Vous pouvez vous inspirer de [codeguide.com](https://codeguide.co/)

## Des outils pour vous aider

  - [stylelint](https://stylelint.io) : Un linter puissant et moderne qui vous aide à éviter les erreurs et à appliquer les conventions dans vos styles.
  - [postcss](https://postcss.org) : Augmenter la lisibilité du code, évitez les erreurs dans votre CSS, optimisez votre code et Utilisez le CSS de demain dès aujourd'hui !

## Ressources

  - [Speaker Deck "Managing CSS Projects with ITCSS" - Harry Roberts](https://speakerdeck.com/dafed/managing-css-projects-with-itcss)
  - [Conférence "Managing CSS Projects with ITCSS" - Harry Roberts](https://www.youtube.com/watch?v=1OKZOV-iLj4&t)
  - [Article "ITCSS: scalable and maintainable CSS architecture" - Lubos Kmetko](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/)

# Synthese3

Synthèse de tous les cours du Bloc 3

# Comment contribuer

## Installer le site en local sur votre machine

1. Installer jekyll en local

Pour cela vous aurez besoin d'installer ruby, rubygem.

-   sur window, suivez cette procedure

Télécharger [ruby+Devkit 3.1.3-1 (x64)](https://rubyinstaller.org/downloads/)

Puis choisissez l'option 3 : **MSYS2 and MINGW development toolchain** lors de
l'installation des composants ruby

A la racine du projet, installer le bundler jekyll via cette commande

```
gem install jekyll bundler
```

Verifier si jekyll est bien install

```
jekyll -v
```

-   sur linux, suivez la
    [procédure d'installation](https://jekyllrb.com/docs/installation/ubuntu/)
    via la documentation de jekyll

2. builder le site


Installez les themes présents dans le Gemfile à la racine du dossier exécutez la commande suivante

```
bundle install
```

Toujours à la racine du projet builder le site:  entrez les commandes suivantes:

```
jekyll build
```

puis pour lancez le site en local

```
jekyll serve --trace
```

### Rajouter une page de documentation

Lorsque vous créer une page dans un dossier qui correspond à un module,
spécifier au début du fichier le parent de celui-ci

Ex: Dans le fichier `/TDS/theorie/dilatation_erosion.md` on a :

```
---
title: Dilation Erosion
parent:TDS
---
```

Le parent correspond au title du fichier /tds.md

```
---
title: TDS
nav_order: 2
has_children: true
---
```

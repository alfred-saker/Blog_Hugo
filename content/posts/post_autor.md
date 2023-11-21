+++ 
draft = false
date = 2023-11-20T12:54:53+01:00
title = "Resumé du cours de Hugo Github Pages"
description = ""
slug = ""
authors = ["Alfred Saker"]
tags = ["Dev","Web","Backend","Fullstack","Devops","Github","Hugo"]
categories = []
externalLink = ""
series = []
+++

# HUGO GITHUB PAGES
![Image illustrative](https://www.tomasbeuzen.com/post/making-a-website-with-hugo/featured_hu40cbd56aa319431e2f94c340d268efa8_55522_720x0_resize_lanczos_3.png)

## Introduction

 Hugo est un générateur de sites Web statiques rapide et flexible écrit en Go. Contrairement aux systèmes de gestion de contenu dynamiques, Hugo crée des sites statiques, ce qui signifie que le contenu est généré avant d'être publié sur le serveur. Cela permet une performance optimale, une sécurité accrue, et une facilité de déploiement.

GitHub Pages, quant à lui, est un service d'hébergement gratuit proposé par GitHub qui permet de publier des sites Web directement depuis des dépôts GitHub. Il prend en charge les sites Web statiques, en faisant de lui un choix idéal pour héberger des sites générés par Hugo.

## C'est quoi HUGO?

 Hugo est un générateur de sites Web open-source écrit en langage de programmation Go (golang). Il permet de créer des sites Web statiques, ce qui signifie que le contenu du site est généré à l'avance plutôt que d'être généré dynamiquement lorsqu'un utilisateur accède au site.

## Installation et Utilisation de HUGO

Afin d'utiliser Hugo , il faut installer au préalable HUGO et GIT

### 1.Installation de HUGO
+ Windows : [insatllation Hugo sur Windows](https://gohugo.io/installation/windows/)
+ Linus : [insatllation Hugo sur MacOs](https://gohugo.io/installation/macos/)
+ MacOs : [Installation Hugo sur Linus](https://gohugo.io/installation/linux/)

Etant donnée que j'utilise **Windows**, nous allons utilise cette commande qui installera la version etentue de Hugo:

![Image illustrative](https://community.chocolatey.org/content/images/global-shared/logo-square.svg)

`Chocolated` est un gestionnaire de package windows , il est installé par défaut avec le système windows. Pour plus d'information [chocolated](https://community.chocolatey.org/)

`choco install hugo-extended`

### 2.Installation de Git
L'installation de git se fait juste en executant le fichier **.exe** que vous retrouvez sur le [site officiel](https://git-scm.com/).

## Premier pas avec HUGO
Une fois l'environnement prêt vous pouvez commencer par la creation de votre premier site avec Hugo.
* Creation d'un site :
  + `hugo new site quickstart` : Creation d'un nouveau site
  + ``cd quickstart``: Acceder au dossier du site
  + ``git init`` : Initialiser le dossier comme un depôt git
  + ``git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke`` : Installer le thème de votre choix dans le dossier. Pour plus de choix , selectionner votre thème [ici](https://themes.gohugo.io/)
  + ``echo "theme = 'ananke'" >> hugo.toml``: Spécifier le thème utiliser; Cette action peut aussi être réaliser dans le fichier Hugo.toml qui se situe a la racine de votre dossier. 
  + ``hugo server`` : Enfin lancer le server pour visualiser votre premier site en local ✌️

Félicitations!! Vous venez de creer votre premier site statique avec Hugo!🎉🎊

> Pour une personnalisation plus approfondie du thème choisi, il est préférable de consulter les fichiers de configuration du thème qui se trouve sur le depot de son créateur!

Jusqu'a maintenant notre site est uniquement héberger en local, nous désirons l'heberger sur Github. Pour le faire, creer un repository dans votre compte guthub et tapé les commandes suivantes:
+ ``git init``
+ ``git add README.md``
+ ``git commit -m "first commit"``
+ `` git branch -M main``
+ ``git remote add origin https://github.com/alfred-saker/sd.git``
+ ``git push -u origin main`` 

Une fois cette etape fait, il faut bien evidement, automatiser les changements qui se feront sur notre site pour eviter de repeter les mêmes commandes.

Rendez-vous dans votre repository sur github:

setting > pages > Github action et ensuite choisissez Hugo

Ensuite validez le commit changes et un fichier *.yaml* va se creer automatiquement et c'est grace à se fichier que notre site sera visible en ligne. 

Apres cela, on va devoir modifié l'url de notre thème et le pointer vers notre depot github. Faut juste aller dans hugo.toml et changer le contenu de la variable *base_url* en mettant notre propre url. 

une fois cela fait, exécuter les commandes suivantes:

- `Hugo -D` : pour recréer le fichier de configuration Hugo
- `git commit -am 'commentaire'`
- `git push`
- Attendre 1 à 2 min pour que les modifications soient prises en compte
- Retourner dans la section page sur notre compte github et ensuite cliquer sur *Voir le site*

Encore Bravo, nous avons mis en place un site d'automatisation pour la mise en ligne d'un site statique avec Github page et Hugo

Pour ce qui est des changements de couleurs etc.. cela se fait dans les fichiers statiques du thème.


Voila en gros ce que j'ai retenu de ce cours!!



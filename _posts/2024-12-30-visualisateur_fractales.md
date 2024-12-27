---
title: "[Art] Visualisateur de fractales en Javascript"
date: 2024-12-30
---

![Représentation de l'ensemble de Julia pour va valeur -0.8 + 0.156i](https://fr.wikipedia.org/wiki/Ensemble_de_Julia#/media/Fichier:Julia-Menge_-0.8_0.156i.png "Ensemble [-0.8+0.156i] de Julia par PantheraLeo1359531 - Page Wikipedia des ensembles de Julia")

# Idée Générale

Il y a quelques années, je m'étais amusé à faire un visualiseur en Javascript des fractales issues des [ensembles de Julia](https://fr.wikipedia.org/wiki/Ensemble_de_Julia). J'aimerais généraliser l'idée à un ensemble plus large de fonctions issues de calculs de chaos déterministes. Il est par exemple possible de calculer des fractales pour le [problème du pendule et des 3 aimants](https://jacquet.xyz/fractales/). Le problème principal de faire ce type de calcul en Javascript est le temps de calcul parfois nécessaire à la création des images. En 2013, j'avais utilisé la notion de webworkers (sorte de threads pour JS) pour des calculs parallèles sans avoir de lags/freezes de la page web.

Ensemble des fonctionnalités à intégrer :
* Génération des images en client web.
* Calcul des fonctions en utilisant des webworkers
* Rendu dépendant de la fonction appelée
* Panneau de contrôle du rendu dépendant de la fonction. Par exemple la valeur appelée pour une fonction de Julia
* Zoom in et annulation du zoom intégré au visualiseur.
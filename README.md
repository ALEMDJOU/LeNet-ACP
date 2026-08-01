# Classification Fashion-MNIST avec LeNet, ACP et approche hybride

Ce dossier contient un notebook Jupyter dédié à la comparaison de trois stratégies de classification sur la base Fashion-MNIST :

1. un réseau convolutif de type LeNet,
2. une approche basée sur l’Analyse en Composantes Principales (ACP) suivie d’un réseau dense,
3. une approche hybride combinant CNN et ACP.

L’objectif est d’évaluer et de comparer les performances de ces méthodes sur une tâche de classification multi-classes en 10 classes.

---

## Structure du dossier

- [LeNet_Fashion_MNIST_HYBRID.ipynb](LeNet_Fashion_MNIST_HYBRID.ipynb) : notebook principal contenant le pipeline complet d’entraînement et d’évaluation.
- [comparison_3_approches.png](comparison_3_approches.png) : graphique de comparaison des trois approches.
- [confusion_matrices_3_approches.png](confusion_matrices_3_approches.png) : matrices de confusion générées par le notebook.
- fashion-mnist_train.csv : jeu de données d’entraînement à placer dans ce dossier.
- fashion-mnist_test.csv : jeu de données de test à placer dans ce dossier.

---

## Objectif du projet

Le notebook permet de :

- charger les données Fashion-MNIST à partir de fichiers CSV,
- normaliser les pixels dans l’intervalle $[0, 1]$,
- entraîner trois modèles différents,
- mesurer leurs performances avec des métriques de classification,
- visualiser les résultats à l’aide de graphiques et de matrices de confusion.

---

## Prérequis

Installer les dépendances suivantes avant d’exécuter le notebook :

```bash
pip install numpy pandas matplotlib seaborn scikit-learn tensorflow jupyter
```

Le projet est conçu pour fonctionner avec une configuration mémoire modérée, sans GPU.

---

## Données requises

Le notebook attend les fichiers suivants dans le même dossier :

- fashion-mnist_train.csv
- fashion-mnist_test.csv

Sans ces fichiers, l’exécution du notebook ne pourra pas démarrer correctement.

---

## Exécution

1. Ouvrir le notebook dans Jupyter ou dans VS Code.
2. Exécuter les cellules dans l’ordre.
3. Observer les résultats des trois approches ainsi que les graphiques générés.

---

## Approches étudiées

### 1. LeNet standard (CNN pur)

Architecture convolutive classique appliquée directement aux images d’entrée.

### 2. ACP + réseau dense

Les images sont d’abord réduites en dimension par ACP, puis classées par un réseau dense.

### 3. Approche hybride CNN + ACP

Cette méthode combine l’extraction de caractéristiques par CNN avec une réduction de dimension par ACP avant la classification finale.

---

## Résultats attendus

Le notebook produit :

- les rapports de classification,
- les matrices de confusion,
- des comparaisons visuelles entre les approches.

---

## Notes

- Les données sont traitées sous forme d’images 28×28 pixels.
- Les étiquettes correspondent aux 10 classes du jeu Fashion-MNIST.
- Des graines aléatoires fixes sont utilisées pour améliorer la reproductibilité.

---

## Contexte

Ce travail s’inscrit dans un projet d’apprentissage profond visant à comparer différentes stratégies de classification d’images, notamment CNN, ACP et méthodes hybrides.

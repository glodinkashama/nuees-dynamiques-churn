# Algorithme des Nuées Dynamiques – Analyse du Churn

## 1. Présentation

Ce projet porte sur l'implémentation de l'algorithme des nuées dynamiques à partir d'un jeu de données de clients d'un opérateur téléphonique.

L'objectif est de constituer des groupes homogènes de clients à partir de leurs caractéristiques d'utilisation des services téléphoniques, puis d'analyser la répartition du churn entre les groupes obtenus.

## 2. Données

Le jeu de données contient 2 667 observations et 16 variables.

La variable `Churn.` indique si le client a quitté ou non le service.

La variable `Phone`, utilisée comme identifiant, n'est pas utilisée pour la classification.

## 3. Méthode

L'algorithme des nuées dynamiques est implémenté à partir de zéro, sans utiliser une fonction de clustering de `scikit-learn`.

Les principales étapes sont :

1. préparation des données ;
2. sélection des variables quantitatives ;
3. standardisation des variables ;
4. initialisation des prototypes ;
5. affectation des observations au prototype le plus proche ;
6. recalcul des prototypes ;
7. répétition jusqu'à convergence ;
8. évaluation des partitions obtenues.

La distance utilisée est la distance euclidienne.

## 4. Nombre de groupes

Plusieurs valeurs de K sont étudiées :

- K = 2
- K = 3
- K = 4
- K = 5
- K = 6

L'inertie et le coefficient de silhouette sont utilisés pour évaluer les partitions.

Une analyse de stabilité selon plusieurs graines aléatoires est également réalisée.

## 5. Résultats

La solution finale retenue dans le projet comporte 4 groupes.

Les groupes sont ensuite caractérisés à partir de leurs profils de consommation et de leur taux de churn.

## 6. Fichiers

- `nuees-dynamiques-churn.ipynb` : notebook contenant l'implémentation et l'analyse.
- `churn_trainingdataset.csv` : jeu de données utilisé pour l'analyse.

## 7. Exécution

Pour reproduire l'analyse :

1. télécharger ou cloner le dépôt ;
2. installer les dépendances Python nécessaires ;
3. ouvrir le notebook `nuees-dynamiques-churn.ipynb` avec Jupyter Notebook ou JupyterLab ;
4. exécuter les cellules dans l'ordre.

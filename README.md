# OpenClassroom_projet8_House_Prices_Advanced_Regression_Techniques
## House Prices - Advanced Regression Techniques
---
![banner](https://storage.googleapis.com/kaggle-competitions/kaggle/5407/media/housesbanner.png)


## Contexte:

Dans le cas d'achats d'une maison, les caractéristiques de celle-ci qui peuvent déteminer son prix peuvent être inattendues.
C'est pour cela que nous allons chercher à déterminer les prix de maison à l'aide de 79 variables explicatives. Ces variables décrivent
approximativement tous les aspects de la zone résidentielle de la ville Ames. Les données ont été compilées par  Dean De Cock sous le nom de [Ames Housing dataset](http://www.amstat.org/publications/jse/v19n3/decock.pdf). Ce projet [House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques) est une compétition proposé sur le site [Kaggle](https://www.kaggle.com/). Cette compétition est ouvert à tous les membres de la plateforme et n'est pas limité  dans le temps.

## Les données:

Le dataset est composé de 2 fichiers. Un fichier qui contient les données d'entrainement avec le prix des maisons. Ainsi qu'un fichier de données de test qui lui ne contient pas les prix des maisons.

## Traitement Proposé

Dans cette étude nous allons nous limiter dans une première phase à utiliser seulement 35 variables. puis dans un second temps proposer une solution à 43 variables utilisées. Notre première phase de prétraitement consiste à remplacer les valeurs manquantes pour chacune des variables sélectionnées. Nous pouvons donc effectuer un nettoyage des outliers pour chacune des colonnes. le nombre d'outliers considérer sera de 2% dans chaque colonnes.

## Modélisation

Nous avons choisi 5 algorithmes pour prédire le prix des maisons: `Ridge`, `Random Forest` , `Gradient Boosting` , `Xgboost`, `LightGBm`. Une recherche des meilleurs paramètres sera effectuée avec la librairie Scikit-Learn et [Optuna](https://optuna.org/).



## Résultats

les résultats du premier essai avec 35 variables du dataset fourni.
Résultats:

| Algorithmes   | Ridge   | Random Forest | Gradient Boosting | XGboost | LightGBM |
| ------------- |:-------:|:------------:|:-----------------:|:-------:|---------:|
| RMSE          | 22506 	| 30664		      |  25340           | 24817  | 21025   |
 


les résultats sont présentés sur le second essai réalisé avec 43 variables.
Résultats:

| Algorithmes   | Ridge         | LightGBM  |
| ------------- |:-------------:| ---------:|
| RMSE          | 20369 				 | 18941 		|


Le meilleur résultat obtenu est LIghtGBM avec une RMSE de 18941 \$


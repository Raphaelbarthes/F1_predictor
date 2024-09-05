# Projet-Python-pour-le-Data-Scientist : Formula@1

Bienvenue sur le Github de notre projet Python Pour le Data Scientist de @milanhurtado, @IdrissKad et @Va2944.

L'objectif de ce projet est de prédire la victoire sur le prochain Grand Prix de Formule 1.

Pour cela, nous avons utlisé les données des Grands Prix de 1990 à 2020 (nous avons choisi de manière arbitraire de ne pas sélectionner les Grands Prix avant 1990 étant donnés les progrès techniques fulgurants à partir des années 1990) qui sont stockées sur le site Ergast F1 (https://ergast.com/mrd/)

![ErgastF1](Ergast_Présentation.png)

Nous avons procédé en plusieurs étapes : 

## 1. Récupération des données et Datavizualisation

_Objectif 1_ : créer une première base "Races" regroupant les années des saisons, le nom et le rang du circuit dans la saison, la latitude et la longitude du circuit (utile plus tard pour les représentations géographiques), le pays et la date du circuit, ainsi que l'url wikipédia associé

_Objectif 2_ : créer une deuxième base "Result" incluant notamment la position sur la grille de départ et le podium final

_Objectif 3_ : établir des corrélations entre les variables d'intérêt (à titre d'exemple, l'étude de la corrélation entre le classement à la grille de départ et celui à l'arrivée ou la corrélation entre l'âge du pilote et le fait de gagner)

## 2. Modélisation et Entraînement du modèle

_Objectif 1_ - Préparation des données : création d'un dataframe unique dans lequel nous pouvons retrouver toutes les variables a priori utiles pour la modélisation, ainsi que notre target, c'est à dire le vainqueur de la course (ou un proxy : le classement de la course) : merge des dataframes et gestion des valeurs manquantes

_Objectif 2_ - Classification : Pour prédire le gagnant d'un grand prix de F1, nous pouvons procéder par classification en considérant que le gagnant est de la catégorie 1 et le perdant de la catégorie 0.

_Objectif 3_ - Entraînement du modèle : Pour évaluer la performance de notre modèle, nous avons décidé d'entraîner notre modèle sur les années précédants 2020 et de mesurer la performance de notre modèle comme le pourcentage de course "bien" prédite en 2020. Il existe d'autres approches mais nous avons choisie cette dernière car elle permet d'évaluer intuitivement la pertinence ou non du modèle sur une année récente.

_Objectif 4_ : Comapraison des modèles de classification et de régression linéaire 

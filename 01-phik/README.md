# Note technique 01 — Classer les variables tarifaires 

Comparaison de deux façons de sélectionner les variables explicatives
d'un modèle de fréquence et de coût moyen, sur un portefeuille
automobile aux variables de types mélangés.

**Lecture en ligne :** https://Rayarn.github.io/notes-techniques/01-phik/

## Ce que fait le carnet

- Construit deux cibles tarifaires : fréquence annualisée et coût moyen.
- Classe 18 variables explicatives face à chaque cible avec le
  coefficient phi-K, puis avec les méthodes classiques : Pearson,
  Spearman, rapport de corrélation, V de Cramér.
- Mesure les dépendances entre les 153 couples d'explicatives selon
  les deux approches et isole les couples sur lesquels elles divergent.

## Ce qu'il ne fait pas

Aucun modèle n'est estimé. phi-K est un indicateur de tri : il donne
l'intensité d'une dépendance, jamais son sens, et il ne dispense
d'aucun test au sein du modèle.

## Exécution

pip install -r requirements.txt
jupyter lab
note01_phik_freMPL3.ipynb


Le jeu de données est téléchargé au premier lancement. La matrice de 
significativité repose sur des simulations de Monte-Carlo et prend
quelques minutes.

`charte_notebook.css` doit rester dans le même dossier que le carnet.

## Sources

- Données : freMPL3, CASdatasets, C. Dutang et A. Charpentier.
- Méthode : M. Baak, R. Koopman, H. Snoek, S. Klous, *A new correlation
  coefficient between categorical, ordinal and interval variables with
  Pearson characteristics*, arXiv:1811.11440, 2019.
- Implémentation : https://phik.readthedocs.io

## Auteur

Arnaud MBARGA


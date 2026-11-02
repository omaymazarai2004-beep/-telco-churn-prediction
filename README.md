# Prédiction du désabonnement de clients télécoms (Churn)

Projet de machine learning supervisé : prédire si un client d'un opérateur télécom va résilier son abonnement.

## Objectif
Identifier les clients à risque de départ à partir de leurs caractéristiques (contrat, ancienneté, facturation, services souscrits).

## Données
- Jeu de données **Telco Customer Churn** (IBM), disponible sur Kaggle : [https://www.kaggle.com/datasets/blastchar/telco-customer-churn?resource=download]
- 7 043 clients, 21 variables. Environ 27 % de clients ont quitté l'opérateur.
- Le fichier CSV n'est pas inclus dans ce dépôt. Téléchargez-le sur Kaggle et placez-le à côté du notebook.

## Méthode
1. Nettoyage des données (valeurs manquantes, variable `TotalCharges`)
2. Analyse exploratoire et visualisations
3. Préparation : normalisation, encodage one-hot, séparation entraînement/test (80/20, stratifiée)
4. Comparaison de trois modèles par validation croisée : régression logistique, Random Forest, Gradient Boosting
5. Évaluation sur le jeu de test : F1-score, AUC, matrice de confusion, courbe ROC
6. Interprétation : importance des variables

## Résultats
| Modèle | F1 (test) | AUC (test) |
|---|---|---|
| Régression logistique | [0.614] | [0.842] |
| Random Forest | [0.537] | [0.823] |
| Gradient Boosting | [0.581] | [0.843] |

Meilleur modèle : **[Gradient Boosting]**.
Facteurs les plus liés au départ : [TotalCharges, tenure, MonthlyCharges].

## Technologies
Python, pandas, NumPy, scikit-learn, matplotlib, seaborn, Jupyter Notebook

## Exécution
1. Installer les dépendances : `pip install pandas numpy matplotlib seaborn scikit-learn jupyter`
2. Télécharger le CSV depuis Kaggle et le placer dans le même dossier que le notebook
3. Ouvrir `Telco_Churn_Oumayma_ZARAI.ipynb` et exécuter les cellules dans l'ordre (ou l'ouvrir dans Google Colab)

## Auteure
Oumayma ZARAI, étudiante ingénieure en informatique à l'ENSIT
[linkedin.com/in/zarai-oumayma-]

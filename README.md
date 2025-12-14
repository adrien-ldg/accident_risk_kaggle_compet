# 🚦 Classification de la gravité des accidents routiers (Kaggle)

<!-- Badges compétences -->

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg?logo=python\&logoColor=white)](https://www.python.org/)
[![pandas](https://img.shields.io/badge/pandas-Data%20Analysis-purple?logo=pandas\&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-lightblue?logo=numpy\&logoColor=white)](https://numpy.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-Machine%20Learning-orange?logo=scikitlearn\&logoColor=white)](https://scikit-learn.org/)
[![Kaggle](https://img.shields.io/badge/Kaggle-Competition-20BEFF?logo=kaggle\&logoColor=white)](https://www.kaggle.com/)

---

## 🎯 Contexte

Projet mené dans le cadre d’une compétition Kaggle visant à prédire la **gravité des accidents de la route en France**. Le jeu de données comprend plus de **80 variables hétérogènes** (localisation, conditions météorologiques, environnement, caractéristiques du véhicule et de l’usager). L’objectif principal était de construire une **pipeline de Machine Learning robuste**, depuis la préparation des données jusqu’à l’évaluation comparative de plusieurs modèles prédictifs.

Ce projet met l’accent sur la **qualité du feature engineering**, la rigueur et l’analyse des performances des modèles.

## 🚀 Rejouer le projet

Télécharger le jeu de données Kaggle « Gravité des accidents » (mêmes fichiers que ceux utilisés durant la compétition) et le placer à la racine du projet, ou adapter les chemins d’accès dans les notebooks.

Créer ensuite un environnement virtuel et installer les dépendances à partir du fichier `requirements.txt`, incluant notamment **Python, Jupyter, pandas et scikit-learn** :

```bash
python -m venv .venv
source .venv/bin/activate  # Sous Windows : .venv\\Scripts\\activate
pip install --upgrade pip
pip install -r requirements.txt
```

Lancer Jupyter et ouvrir les notebooks :

```bash
jupyter notebook
```

* `notebook_feature_adrien_lindeberg.ipynb` : pipeline complet de feature engineering
* `notebook_remis.ipynb` ou `notebook_model_adrien_lindeberg.ipynb` : entraînement, comparaison et évaluation des modèles

## 🛠️ Feature engineering et préparation des données

La préparation des données constitue une étape centrale du projet. Elle débute par un **nettoyage approfondi et un typage strict** des variables (dates, catégories, variables numériques), ainsi qu’un traitement  des valeurs manquantes afin de garantir la cohérence du jeu de données.

Les variables catégorielles sont transformées en représentations numériques adaptées aux algorithmes de Machine Learning (encodage one-hot ou binaire). Les variables continues sont **standardisées** pour éviter tout biais lié aux différences d’échelle.

Une phase de **réduction de dimensionnalité** est ensuite appliquée : suppression des variables redondantes, faiblement informatives ou fortement corrélées. Cette étape permet de réduire l’espace de features d’une quarantaine de variables initiales à **environ 20 variables pertinentes**, tout en conservant l’essentiel de l’information prédictive.

Enfin, un **découpage train/validation** est réalisé afin d’évaluer la capacité de généralisation des modèles avant l’entraînement final.

## 🤖 Modélisation et algorithmes explorés

Plusieurs familles de modèles supervisés ont été implémentées et comparées :

* **Arbres de décision** et méthodes de bagging, utilisés comme modèles de référence pour leur interprétabilité.
* **RandomForest** et autres méthodes d’ensemble, afin d’améliorer la robustesse et réduire la variance.
* **Méthodes de boosting** (Gradient Boosting / XGBoost), testées pour leur capacité à capturer des interactions complexes entre les variables.
* **Réseaux de neurones simples**, utilisés comme point de comparaison avec des approches plus classiques.

L’évaluation repose sur plusieurs métriques (précision, rappel, F1-score et AUC-ROC) afin d’obtenir une vision complète des performances.

## 📊 Résultats finaux

> **Meilleur modèle retenu : Boosting (Gradient Boosting / XGBoost)**

| Métrique     | Score     |
| ------------ | --------- |
| 🎯 Précision | **0.814** |
| 🔁 Recall    | **0.746** |
| ⚖️ F1-score  | **0.779** |
| 📈 AUC-ROC   | **0.901** |

Ces performances mettent en évidence une **forte capacité de discrimination** du modèle, ainsi qu’un **équilibre pertinent entre rappel et précision**, critère clé pour une tâche de classification de gravité.

---

## ✅ Conclusion et compétences acquises

Ce projet a permis de mettre en œuvre un **pipeline complet de Machine Learning**, depuis la préparation des données jusqu’à l’optimisation et l’évaluation des modèles. Il illustre l’importance du **feature engineering** et du choix des algorithmes dans une problématique de classification.

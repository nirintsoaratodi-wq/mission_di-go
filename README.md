# 📚 Formation Data Science — 2025

Bienvenue dans ce dépôt ! Il rassemble l'ensemble des ressources, supports et travaux pratiques que j'ai conçus et dispensés dans le cadre de ma **formation en Data Science** au cours de l'année **2025**.

Ce projet reflète mon travail en tant que **formateur**, depuis la conception des cours et exercices Python jusqu'à la mise en place de cas pratiques en Machine Learning, en passant par les statistiques, la visualisation de données et le déploiement de modèles.

---

## 🗂️ Structure du projet

```
Formation/
│
├── Cours/                  # Supports de cours et travaux pratiques conçus
│   ├── Introduction à Python pour la Data Science
│   ├── TP Python Fondamental
│   ├── TP Python++
│   └── TP Neural Network
│
├── notebook/               # Notebooks de démonstration et d'exercices
│   ├── Pratique_de_classification.ipynb
│   ├── Pratique_de_regression.ipynb
│   ├── Pratique_de_clustering.ipynb
│   ├── Pratique_serie_temporelle.ipynb
│   ├── Etaps_ML.ipynb
│   ├── stats.ipynb
│   └── ...
│
├── data/                   # Jeux de données fournis pour les exercices
│   ├── diabetes.csv
│   ├── titanic.xlsx
│   ├── meteo.csv
│   ├── jewellery.csv
│   ├── insurance.xlsx
│   ├── Passenger.csv
│   └── new_data.xlsx
│
├── model/                  # Modèles entraînés servant d'exemples (.pkl)
│   ├── modele_classification.pkl
│   ├── modele_regression.pkl
│   ├── model_de_clustering.pkl
│   └── model_de_serieTemp.pkl
│
├── Evaluation/             # Évaluations et grilles de notation
├── Rapport/                # Rapports de mission de formation
├── reports/                # Programme de formation et ressources
├── modul1/                 # Module 1 — Fondamentaux Python
├── virtuel/                # Environnement virtuel Python
└── requirements.txt        # Dépendances du projet
```

---

## 🎯 Objectifs pédagogiques

Cette formation a été pensée pour accompagner les apprenants dans leur montée en compétences sur les thématiques suivantes :

- **Les bases de Python** appliquées à la Data Science
- **Les statistiques** descriptives et inférentielles
- **L'exploration et la préparation des données** (nettoyage, feature engineering, encodage)
- **La construction de modèles de Machine Learning** :
  - Classification (ex. : détection du diabète, survie du Titanic)
  - Régression (ex. : prédiction d'assurance)
  - Clustering (ex. : segmentation de données bijouterie)
  - Séries temporelles (ex. : prévisions météo)
- **L'évaluation et la sauvegarde des modèles** pour une utilisation en production
- **L'initiation au déploiement** de modèles ML avec Flask et MLflow

---

## 🛠️ Technologies et outils utilisés

| Catégorie | Outils |
|-----------|--------|
| **Langage** | Python 3 |
| **Data** | Pandas, NumPy |
| **Visualisation** | Matplotlib, Plotly, Dash |
| **Machine Learning** | Scikit-learn, LightGBM, Imbalanced-learn |
| **Séries temporelles** | Statsforecast |
| **Deep Learning** | Réseaux de neurones (TP Neural) |
| **Tracking ML** | MLflow |
| **Déploiement** | Flask |
| **Notebooks** | Jupyter / IPython |

---

## 🚀 Installation et utilisation

### 1. Cloner le dépôt

```bash
git clone <url-du-depot>
cd Formation
```

### 2. Créer un environnement virtuel

```bash
python -m venv virtuel
# Windows
virtuel\Scripts\activate
```

### 3. Installer les dépendances

```bash
pip install -r requirements.txt
```

### 4. Lancer les notebooks

```bash
jupyter notebook
```

Ouvrez les notebooks dans le dossier `notebook/` pour parcourir les démonstrations et les exercices pratiques.

---

## 📊 Contenu pédagogique

### Classification
Exercices et démonstrations autour de la prédiction de résultats binaires ou multi-classes. Techniques abordées : KNN, arbres de décision, validation croisée, grid search.

### Régression
Cas pratiques de modélisation de variables continues. Entraînement et évaluation avec des métriques comme le RMSE et le R².

### Clustering
Initiation à la segmentation non supervisée. Application de K-Means et exploration de groupes naturels dans les données.

### Séries temporelles
Analyse de données temporelles, détection de tendances et saisonnalité, prévisions avec des modèles statistiques.

---

## 👤 Auteur

**Nirintsoa** — Formateur en Data Science, 2025.

> *Ce dépôt est le fruit de mon travail de conception pédagogique. Il regroupe tous les supports, exercices et ressources que j'ai préparés pour transmettre les compétences en Data Science à mes apprenants.*

---

## 📄 Licence

Ce projet est à usage éducatif.

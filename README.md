# Prévision de la Qualité de l'Air avec Deep Learning

## Description

Projet d'analyse et de prévision de la pollution atmosphérique utilisant des techniques de deep learning appliquées à des données temporelles. Ce projet exploite des réseaux de neurones récurrents (LSTM et GRU) pour prédire les concentrations de polluants atmosphériques, notamment le dioxyde d'azote (NO2), en se basant sur des données historiques de qualité de l'air.

## Objectifs

- Analyser les tendances de pollution atmosphérique sur une période d'un an
- Identifier les facteurs influençant la qualité de l'air
- Développer des modèles prédictifs performants pour anticiper les niveaux de pollution
- Comparer les performances de différentes architectures de réseaux de neurones récurrents

## Dataset

**Source :** [Air Quality UCI Dataset](https://archive.ics.uci.edu/ml/datasets/Air+Quality) (disponible sur Kaggle)

**Caractéristiques :**
- Période : Mars 2004 - Février 2005 (1 an complet)
- Localisation : Zone urbaine à proximité d'une route, Rome, Italie
- Fréquence : Enregistrements horaires
- Variables : Concentrations de divers polluants (NO2, CO, NOx, etc.) et conditions météorologiques

## Technologies Utilisées

- **Python 3.x**
- **Pandas & NumPy** : Manipulation et analyse des données
- **Matplotlib & Seaborn** : Visualisation des données
- **Scikit-learn** : Prétraitement et métriques d'évaluation
- **TensorFlow/Keras** : Construction des modèles de deep learning
  - LSTM (Long Short-Term Memory)
  - GRU (Gated Recurrent Unit)

## Méthodologie

### 1. Prétraitement des Données
- Nettoyage du dataset (gestion des valeurs manquantes)
- Sélection des variables numériques pertinentes
- Normalisation avec MinMaxScaler
- Création de séquences temporelles pour les modèles récurrents

### 2. Analyse Exploratoire
- Visualisation des tendances temporelles
- Analyse des corrélations entre polluants
- Identification des patterns saisonniers

### 3. Modélisation
- **Architecture LSTM** : Capture des dépendances à long terme
- **Architecture GRU** : Alternative plus légère au LSTM
- Utilisation de Dropout pour éviter le surapprentissage
- Early Stopping pour optimiser l'entraînement

### 4. Évaluation
- Validation croisée temporelle (TimeSeriesSplit)
- Métriques : RMSE, MAE, R², MAPE
- Comparaison des performances entre modèles

## Métriques d'Évaluation

Les modèles sont évalués selon plusieurs critères :
- **RMSE** (Root Mean Square Error) : Erreur quadratique moyenne
- **MAE** (Mean Absolute Error) : Erreur absolue moyenne
- **R²** : Coefficient de détermination
- **MAPE** (Mean Absolute Percentage Error) : Erreur en pourcentage

## Utilisation

### Prérequis
```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow
```

### Exécution
1. Télécharger le dataset `AirQualityUCI.csv`
2. Placer le fichier dans le même répertoire que le notebook
3. Ouvrir `ProjetDeSynthèse.ipynb` dans Google Colab ou Jupyter Notebook
4. Exécuter les cellules séquentiellement

## Structure du Projet

```
ProjetDeSynthèse/
│
├── ProjetDeSynthèse.ipynb    # Notebook principal
├── AirQualityUCI.csv          # Dataset (à télécharger)
└── README.md                  # Documentation
```

## Résultats

Le projet compare les performances de deux architectures de réseaux de neurones récurrents (LSTM et GRU) sur la prévision de la concentration de NO2. Les résultats incluent :
- Courbes d'apprentissage (loss)
- Prédictions vs valeurs réelles
- Comparaison statistique des performances
- Analyse de la validation croisée

## Recherches Existantes

Le projet s'appuie sur des recherches existantes dans le domaine de la prévision de la qualité de l'air et identifie les principaux facteurs influençant la pollution atmosphérique en milieu urbain.

## Auteur

**Votre Nom**  
Étudiant en Baccalauréat en Informatique Option science de données 
[www.linkedin.com/in/inzaghif]

## Licence

Ce projet a été réalisé dans un cadre académique.

---

*Projet réalisé dans le cadre du stage 1 de mon programme

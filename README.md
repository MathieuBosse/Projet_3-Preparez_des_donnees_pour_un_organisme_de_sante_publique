# 🧹 Projet de Nettoyage et Exploration des Données Open Food Facts

## 🧠 Contexte

Ce projet a été réalisé dans le cadre d'une mission pour **Santé publique France**, avec pour objectif d'améliorer la qualité des données de la base **Open Food Facts**, une base collaborative sur les produits alimentaires.

La problématique principale : les champs à remplir lors de l’ajout d’un produit sont nombreux et souvent sujets à erreurs ou oublis. L’idée est donc de :

- **Nettoyer les données existantes** (valeurs aberrantes, manquantes, doublons, etc.)
- **Analyser les données** pour identifier des patterns
- **Créer un système de suggestion automatique** des valeurs manquantes, basé sur des produits similaires

---

## ⚙️ Méthodologie

Le projet a été mené en plusieurs étapes :

### 1. Nettoyage des données
- Suppression des colonnes inutiles (dates, liens, etc.)
- Détection et suppression des doublons
- Correction des erreurs : valeurs impossibles (ex. >100g/100g), remplacées par `NaN`
- Vérification de la cohérence (ex. somme des nutriments ≤ 100g)

### 2. Remplissage des valeurs manquantes
- Imputation des données manquantes par **médiane** des produits du **même groupe alimentaire**

### 3. Analyse exploratoire
- Moyennes et distributions des nutriments (énergie, glucides, fibres, etc.)
- Étude des corrélations entre les variables (ex. graisses ↔ énergie, glucides ↔ sucres)
- Tests statistiques (ANOVA, Khi²) pour vérifier l’impact du groupe alimentaire

### 4. Prototype de suggestion automatique
- À partir d’un champ renseigné (ex. 60g de glucides pour un biscuit), le système propose des estimations pour d'autres (ex. sucres ≈ 25g, énergie ≈ 1700 kJ)

---

## ✅ Résultats

- **Nettoyage efficace** : moins de valeurs manquantes ou incohérentes
- **Analyses cohérentes** avec les connaissances nutritionnelles
- **Prototype fonctionnel** pour prédire des champs manquants à partir de produits similaires

---

## 🚀 Perspectives

- Ajouter plus de produits pour enrichir les prédictions
- Intégrer l’outil dans l’interface de saisie d’Open Food Facts
- Effectuer des tests utilisateurs
- Assurer la conformité RGPD (pas de données personnelles utilisées)

---

## 📁 Fichiers du projet

- `cleaning.ipynb` : Nettoyage des données
- `analysis.ipynb` : Analyse exploratoire et statistiques
- `suggestion_system.ipynb` : Prototype de suggestion automatique
- `data/` : Données brutes et nettoyées

---

## 🧪 Outils et Librairies

- Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, SciPy)
- Jupyter Notebooks

---

## 📬 Contact

Si vous avez des questions ou des suggestions :  
**Auteur : [Ton Prénom / Nom]**  
**Email : [ton.email@example.com]**

---

## ⭐ Remerciements

Merci à **Santé publique France** pour la confiance et à la communauté **Open Food Facts** pour leur contribution à une alimentation plus transparente.


# 🌿 Analyse de la Variance à Trois Facteurs (ANOVA 3-Facteurs) sous R

## 📘 Description du projet
Ce projet implémente une ANOVA à trois facteurs. L’objectif est d’analyser l’effet combiné de l’origine géographique des plantes (`Type`), du traitement thermique (`Treatment`) et de la concentration en CO₂ (`conc`) sur leur capacité photosynthétique (`uptake`). L’étude inclut la vérification des hypothèses, des visualisations, et une interprétation détaillée des résultats.

## 🧪 Objectifs
- Quantifier l’effet de chaque facteur pris isolément
- Identifier les interactions à deux et trois facteurs
- Vérifier les hypothèses de l’ANOVA (normalité, homogénéité des variances)
- Réaliser des tests post-hoc avec correction (Tukey HSD)

## 📁 Structure du dépôt

## 🧰 Technologies utilisées
- Langage : **R**
- Packages :
  - `ggplot2` pour les visualisations
  - `car` pour le test de Levene
  - `emmeans` pour les comparaisons post-hoc et moyennes marginales

## 📊 Données
- Jeu de données : `CO2` (intégré à R)
- Variables :
  - `uptake` : taux de fixation du CO₂ (quantitative)
  - `Type` : origine géographique (`Quebec`, `Mississippi`)
  - `Treatment` : condition thermique (`chilled`, `nonchilled`)
  - `conc` : concentration en CO₂ (transformée en facteur)

## 🔍 Résultats principaux
- Effets très significatifs des trois facteurs principaux (Type, Treatment, conc)
- Interactions Type × Treatment et Type × conc hautement significatives
- L’interaction triple Type × Treatment × conc proche de la significativité
- Les plantes québécoises présentent une meilleure résilience au stress froid
- L'effet du froid est modulé par la concentration en CO₂

## ✅ Vérification des conditions
- **Homogénéité des variances** : validée par le test de Levene (p = 1)
- **Normalité des résidus** : légère déviation (p ≈ 0.0017), mais ANOVA robuste

## ▶️ Reproduire l’analyse
1. Cloner ce dépôt :
```bash
git clone https://github.com/Baudelaire12/anova3facteurs.git

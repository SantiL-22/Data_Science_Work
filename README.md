# Sleep Health and Lifestyle Analysis 🌙

**Authors:** Santiago López & Aleix Pagès  
**Date:** October 24, 2025  

This repository contains a final Data Science project focused on analyzing a dataset about sleep health and lifestyle (*Sleep Health and Lifestyle Dataset*). The main goal of this work is to understand which daily factors impact sleep quality, using tools for exploratory data analysis, visualization, and statistical modeling developed in `R`.

## 📁 Repository Content

- `Sleep_health_and_lifestyle_dataset.csv`: Original dataset used in the analysis. It consists of 400 observations and 13 variables (age, sleep duration, sleep quality, physical activity level, stress level, BMI category, heart rate, daily steps, sleep disorders, among others).
- `TrabajoDS_Aleix_Santi.Rmd`: R Markdown notebook containing the project's source code, statistical analysis, and plot generation.
- `TrabajoDS_Aleix_Santi.html`: Document generated from the `.Rmd` file that serves as a complete interactive final report, with detailed explanations and conclusions.

## 🎯 Objectives and Methodology

The study develops the following main analytical blocks:

1. **Exploratory Data Analysis (EDA)**: Basic evaluation of data quality (duplicates, NAs, *outliers*) and graphical analysis of distributions for categorical and continuous variables.
2. **Impact of BMI on Sleep**: Formal evaluation (using Kruskal-Wallis and Dunn's Test) of differences in sleep quality according to Body Mass Index category.
3. **Feature Importance**: Regularized regression models (LASSO and Ridge) to empirically identify which variables best explain sleep quality.
4. **Direct Impact of Stress**: Relational and regression analysis focusing on the deep connection between stress levels and a decrease in sleep quality.
5. **Sleep Disorder Prediction**: Logistic Regression algorithm aimed at classifying patients with disorders (Insomnia and Sleep Apnea) based on their physical and psychological stress levels. Performance is evaluated using a ROC curve (AUC: 0.88).
6. **Profile Clustering**: Use of K-Means (optimized with Elbow and Silhouette methods) along with PCA to discover latent patient profiles, thereby identifying different health population groups.

## 📊 Main Conclusions

- There is a very strong **negative correlation (-0.89) between stress level and sleep quality**. It is the factor that most impairs daily rest.
- Physically, there is a notable drop in sleep quality as individuals transition from a "Normal" BMI to an **Overweight or Obese** state.
- Through clustering, **3 latent profiles** are clearly defined: (1) High Stress / Poor Sleep, (2) Good Sleep / Physically Active, (3) Low Physical Activity / Medium Stress.

## 🛠️ Technologies and Libraries Used

The analysis was implemented in the **R** environment, making extensive use of the following libraries:

- **Data Preparation and Transformation**: `dplyr`, `tidyr`, `naniar`, `skimr`
- **Visualization and Exploratory Plots**: `ggplot2`, `corrplot`, `GGally`, `viridis`, `gridExtra`, `scales`
- **Models and Analytical Algorithms**: `caret` (Logistic Regression), `glmnet` (Ridge / Lasso)
- **Unsupervised Learning (Clustering and PCA)**: `FactoMineR`, `factoextra`, `cluster`

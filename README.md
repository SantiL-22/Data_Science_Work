# Análisis de la salud del sueño en relación al estilo de vida 🌙

**Autores:** Santiago López y Aleix Pagès  
**Fecha:** 24 de octubre de 2025  

Este repositorio contiene un proyecto final de Data Science centrado en el análisis de un conjunto de datos sobre la salud del sueño y el estilo de vida (*Sleep Health and Lifestyle Dataset*). El objetivo principal de este trabajo es entender qué factores diarios impactan en la calidad del sueño, utilizando herramientas de análisis exploratorio, visualización y modelos estadísticos desarrollados en `R`.

## 📁 Contenido del Repositorio

- `Sleep_health_and_lifestyle_dataset.csv`: Conjunto de datos original utilizado en el análisis. Está compuesto por 400 observaciones y 13 variables (edad, duración del sueño, calidad del sueño, nivel de actividad física, nivel de estrés, categoría BMI, frecuencia cardíaca, pasos diarios, trastornos del sueño, entre otros).
- `TrabajoDS_Aleix_Santi.Rmd`: Cuaderno en R Markdown con el código fuente del proyecto, análisis estadístico y generación de gráficas.
- `TrabajoDS_Aleix_Santi.html`: Documento generado a partir del `.Rmd` que sirve como informe final interactivo completo, con explicaciones detalladas y conclusiones.

## 🎯 Objetivos y Metodología

El estudio desarrolla los siguientes grandes bloques analíticos:

1. **Análisis Exploratorio de Datos (EDA)**: Evaluación básica de la calidad de los datos (duplicados, NA, *outliers*) y análisis gráfico de distribuciones para variables categóricas y continuas.
2. **Impacto del IMC en el sueño**: Evaluación formal (Mediante pruebas Kruskal-Wallis y Test de Dunn) de las diferencias en la calidad del sueño según la categoría de Índice de Masa Corporal.
3. **Importancia de características**: Modelos de regresión regularizada (LASSO y Ridge) para identificar empíricamente qué variables explican de mejor manera la calidad del sueño.
4. **Impacto directo del Estrés**: Análisis relacional y regresión enfocada en la profunda vinculación entre el nivel de estrés y el descenso en la calidad del sueño.
5. **Predicción de Trastornos**: Algoritmo de Regresión Logística orientado a clasificar pacientes con trastornos (Insomnio y Apnea) en base a su nivel de estrés físico y psíquico. Se evalúa su rendimiento mediante curva ROC (AUC: 0.88).
6. **Agrupación de Perfiles (Clustering)**: Uso de K-Means (optimizado con Elbow y Silhouette) junto a PCA para descubrir perfiles latentes en los pacientes, determinando así distintos grupos poblacionales de salud.

## 📊 Principales Conclusiones

- Existe una fortísima **correlación negativa (-0.89) entre el nivel de estrés y la calidad del sueño**. Es el factor que más perjudica el descanso diario.
- Físicamente, hay una caída destacable de la calidad del sueño a medida que los individuos transitan de un IMC "Normal" a un estado de **Sobrepeso u Obesidad**.
- A través del agrupamiento, se definen **3 perfiles latentes** muy claros: (1) Estrés alto / Sueño bajo, (2) Sueños buenos / Físicamente activos, (3) Baja actividad física / Estrés medio.

## 🛠️ Tecnologías y Librerías Utilizadas

El análisis fue implementado en ambiente **R**, haciendo uso extensivo de las siguientes librerías:

- **Preparación y Transformación**: `dplyr`, `tidyr`, `naniar`, `skimr`
- **Visualización y Gráficos Exploratorios**: `ggplot2`, `corrplot`, `GGally`, `viridis`, `gridExtra`, `scales`
- **Modelos y Algoritmos Analíticos**: `caret` (Regresión Logística), `glmnet` (Ridge / Lasso)
- **Aprendizaje no supervisado (Cluster y PCA)**: `FactoMineR`, `factoextra`, `cluster`

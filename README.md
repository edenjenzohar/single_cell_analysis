# Single-Cell Cancer Classification with Autoencoder Representations
This project demonstrates the development of a machine learning pipeline for classifying single cells as cancerous or non-cancerous, using advanced single-cell RNA sequencing (scRNA-seq) data analysis and representation learning techniques. The approach leverages various methods of dimensionality reduction and representation learning to create meaningful features from scRNA-seq data, followed by training classifiers to predict cell state.

### Project Overview
The goal of this project is to create and evaluate machine learning models that classify single cells based on gene expression profiles, utilizing raw, PCA-transformed, and autoencoder-derived representations. Key objectives include:

Dimensionality reduction and meaningful representation learning with an autoencoder
Comparison of multiple representation strategies to understand their impact on classification performance
Evaluation of classifiers to determine the optimal approach for cancer cell detection

### Methods
#### Data Exploration and Preprocessing
Exploratory Data Analysis (EDA):
Examined scRNA-seq data distributions and filtered out genes and cells based on criteria to improve model training.
Evaluated cell-type heterogeneity and identified relevant features across various samples.
Data Preprocessing:
Normalized gene expression data.
Reduced dimensionality using both PCA and a custom-built autoencoder for generating informative, lower-dimensional embeddings.
Representation Learning

#### Autoencoder:
Built an autoencoder to capture complex patterns in gene expression profiles and create a latent representation for each cell.
Tuned the autoencoder architecture to balance reconstruction accuracy with computational efficiency.
Principal Component Analysis (PCA):

Applied PCA to reduce dimensionality, allowing for a straightforward comparison with the autoencoder embeddings.
Compared the performance of PCA-transformed data with raw and autoencoder representations.
Classification
Using three different types of representations (raw, PCA, and autoencoder-derived), we trained classifiers to distinguish between cancerous and non-cancerous cells.

#### Classifiers:
1. Logistic Regression: Employed logistic regression as a baseline classifier, tuned for balanced performance on imbalanced data.
2. Random forest: Leveraged random forest to capture non-linear relationships, adjusting parameters to prevent overfitting.

Evaluation and Visualization

* Train/Test Splitting by Donor:
Implemented a train/test split based on donor ID to simulate real-world data generalization and to avoid information leakage.
Performance Metrics:

* Evaluated model performance using F1 score, accuracy, and ROC-AUC, providing insights into predictive power and class balance.
SHAP Analysis:

* Conducted SHAP analysis to interpret the feature importance in the classifiers, visualizing top contributing features per cell type to understand decision boundaries.
Results and Conclusions

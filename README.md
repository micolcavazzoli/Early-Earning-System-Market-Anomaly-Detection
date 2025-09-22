# Early-Earning-System-Market-Anomaly-Detection
## Overview
This project, developed for the Fintech course A.Y. 2024/25, implements an Early Warning System for detecting anomalies in financial markets.
The goal is to identify shifts in market regimes (risk-on vs. risk-off) using machine learning techniques, supporting risk management and improving decision-making in times of financial stress.
## Project Aim
- Leverage macroeconomic indices and anomaly labels to build a predictive system
- Compare supervised and unsupervised models
- Apply explainability methods at both local and global levels
- Provide a robust tool for detecting financial anomalies
## Data Preprocessing
- Stationarity test (ADF test)
- Transformations (log differences, simple differences)
- Z-score normalization for feature scaling
## Data Visualization
- 3D UMAP for dimensionality reduction and cluster identification
- Construction of a Global Market Index
- Labeling anomalies as “Up” (positive stress) or “Down” (negative stress)
## Models Implemented
- Multivariate Gaussian Anomaly Detector (MVG): benchmark
- Random Forest: tuned with Optuna (hyperparameter optimization)
- Elliptic Envelope: unsupervised Gaussian-based method
- Autoencoder: deep feed-forward with Batch Normalization
- LSTM Autoencoder: sequential model with dropout + early stopping
## Best Model: LSTM Autoencoder
Precision: 0.92  
Recall: 0.99  
F1 Score: 0.96  
The only model that improved both precision and recall compared to the benchmark. Excellent at capturing temporal dependencies in financial data.
## Explainability
- Local (LIME): shows the most influential features for individual predictions
- Global (Feature Perturbation): evaluates feature importance by reconstruction error variation
Key financial indices (e.g., MSCI Europe Equity Index) emerged as highly relevant, consistent with economic intuition
## Key Findings
Anomalies showed cluster-like patterns in UMAP space  
The LSTM Autoencoder achieved near-perfect performance  
Feature importance analysis aligned with financial reasoning, increasing trust in model outcomes

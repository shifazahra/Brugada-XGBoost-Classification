# **Brugada Syndrome Classification using Morphological ST-Slope Analysis**

This repository contains a machine learning pipeline for the **Binary Classification** of Brugada Syndrome (BrS) vs. Normal ECG signals. The project focuses on high-precision feature engineering to differentiate subtle ECG morphologies.

## Methodology: Preprocessing
To achieve a robust classification, this project implements a specialized pipeline:

* **Signal Cleaning**: Automated flatline detection and 0.5-40Hz Bandpass Filtering to ensure high-quality input.
* **Feature Engineering**: Extraction of **ST-segment Slopes** (Initial & Late) and **J-point amplitudes** to specifically target Type 2/3 Brugada patterns.
* **Handling Class Imbalance**: Applied **SMOTE** oversampling and **GroupKFold** for patient-wise cross-validation to prevent data leakage.
* **Algorithm**: Utilized **XGBoost Classifier** for its superior performance in handling non-linear medical data.

## Classification Results
The model was optimized using an XGBoost Classifier with a threshold of **0.35** to prioritize Sensitivity (Recall):

* **Accuracy**: 88%
* **Recall (Sensitivity)**: 75%
* **F1-Score (Brugada)**: 0.72

## Project Structure
* `Brugada_Classification_XGBoost.ipynb`: Main source code, feature extraction, and model training.
* `requirements.txt`: List of required Python libraries for reproducibility.
* `README.md`: Project documentation and methodology.

## Authors (Team Group)
This project was developed by a team of undergraduate students from **Universitas Singaperbangsa Karawang (UNSIKA)**:

1. **Salsa Anderia Putri Nabila**
2. **Shifa Fanisatuz Zahra**
3. **Najwa Shafa Azahra**

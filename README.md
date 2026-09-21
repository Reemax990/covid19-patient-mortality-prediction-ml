# COVID-19 Patient Mortality Prediction Using Machine Learning

## Overview
This project develops and evaluates machine learning models (Logistic Regression and K-Nearest Neighbor) to predict COVID-19 patient survival outcomes based on demographic, clinical, and pre-existing condition data.

## Dataset
- **Source:** [COVID-19 Dataset](https://www.kaggle.com/datasets/meirnizri/covid19-dataset) by Meir Nizri, Kaggle
- **License:** CC0 Public Domain
- **Size:** ~1,048,575 records, 21 original features
- Data originally provided by the Mexican government

## Files
- `Project__2_.ipynb` — Full analysis notebook (data cleaning, preprocessing, modeling, evaluation)
- `Project_ML-364.pdf` — Full project report
- `README.md` — This file

## Requirements


## Data Preprocessing
1. Removed columns with >80% missing values (`intubed`, `pregnant`, `icu`)
2. Removed rows with missing-value codes (97, 98, 99) in remaining variables
3. Transformed `date_died` into a binary target variable `death` (0 = died, 1 = survived)
4. Balanced classes using Random Undersampling
5. Standardized numerical features using `StandardScaler`
6. Split into 80% training / 20% testing

## Target Variable
`death`: 0 = patient died, 1 = patient survived

## Models & Results
| Model | Accuracy on Validation Data |
|---|---|
| K-Nearest Neighbor (k=6) | 90.11% |
| Logistic Regression | 91.08% |

Logistic Regression performed slightly better in terms of accuracy.

## How to Reproduce
1. Download the dataset from the Kaggle link above
2. Open `Project__2_.ipynb` in Jupyter/Colab
3. Install requirements: `pip install -r requirements.txt`
4. Run all cells in order

## Limitations
- Dataset reflects the Mexican healthcare context and may not generalize to other populations
- Class imbalance was addressed via undersampling, which may discard information
- Results are for academic purposes only and must not be used for clinical decision-making

## Citation
Nizri, M. (2022). *COVID-19 Dataset* [Data set]. Kaggle. https://www.kaggle.com/datasets/meirnizri/covid19-dataset



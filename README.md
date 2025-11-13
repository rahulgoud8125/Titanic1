# Titanic Data — Cleaning & Preprocessing

## Project summary
This repository contains the preprocessing work performed on the Titanic dataset. The goal was to clean the raw data, handle missing values, encode categorical features, scale numerical columns, and remove outliers.

## Files
- `Titanic-Dataset (1).csv` — original raw dataset. (shape: (891, 12))
- `cleaned_data (1).csv` — cleaned dataset produced by the preprocessing steps. (shape: (775, 11))
- `Titanic.py` — Python script used to perform preprocessing (uploaded by the user).
- `README.md` — this file.

## What I did (steps implemented)
1. Removed column: `Cabin` (too many missing values).
2. Dropped rows with missing `Embarked`.
3. For rows with missing `Age`, filled ages using Pclass-based estimates:
   - Pclass 1 -> 38
   - Pclass 2 -> 29
   - Pclass 3 -> 25
4. Concatenated the filled and non-missing subsets back together.
5. Encoded categorical columns:
   - `Sex` and `Embarked` using `LabelEncoder`.
6. Scaled numerical features:
   - `Age` and `Fare` using `StandardScaler`.
7. Visualized `Age` and `Fare` with boxplots (code included).
8. Removed outliers from `Fare` using the IQR method.
9. Saved the cleaned dataset as `cleaned_data (1).csv`.

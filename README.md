# Google Play Store & Apple App Store Analysis

## Overview

This project analyzes app data from Google Play Store and Apple App Store:
- Data cleaning (duplicates, non-English names, free apps)
- Exploratory analysis (most common genres/categories, average ratings/installs)
- Classification models to predict app type (Free vs Paid)
- Saving the final model to `model.h5`

## Files

- `googleplaystore.csv` – raw Android data  
- `AppleStore.csv` – raw iOS data  
- `Playstore-2.ipynb` – analysis notebook  
- `model.h5` – serialized trained model  

## Setup

1. Clone the repository.  
2. Install dependencies:

pip install pandas numpy scikit-learn joblib h5py

text

3. Place both CSV files in the project directory.

## Usage

1. Open `Playstore-2.ipynb` in Jupyter.  
2. Run all cells to:
- Clean and preprocess data  
- Explore app categories, genres, installs, ratings  
- Train and evaluate classifiers  
- Save the trained model  

3. The trained model is saved as `model.h5`.

## Model Deployment

Load the model in a new script:

import joblib

model = joblib.load('model.h5')
Use model.predict(X_new) for new data

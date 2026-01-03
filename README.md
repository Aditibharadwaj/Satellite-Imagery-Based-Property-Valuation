# Multimodal House Price Prediction

This project predicts house prices by combining structured tabular data with satellite image features. It compares traditional tabular-only machine learning models with multimodal models that incorporate visual information extracted from satellite imagery.

The objective is to evaluate whether visual context improves predictive performance over standard regression approaches.

## Project Overview
```
├── data_fetcher.py
├── preprocessing.ipynb
├── model_training.ipynb
├── README.md
```
File Descriptions
- data_fetcher.py: Downloads satellite images using geographic coordinates (latitude and longitude). Images are saved and indexed by property ID.
- preprocessing.ipynb: Performs exploratory data analysis (EDA), tabular data cleaning, feature engineering, image feature extraction using a pretrained CNN, optional PCA, and Grad-CAM–based visual interpretability.
- model_training.ipynb: Trains and evaluates baseline tabular models and multimodal models. Includes pipeline-based preprocessing, model comparison, and prediction on unseen test data.

## Environment Setup
To run this project successfully, ensure the following:
- Python version 3.9 or higher
- A standard scientific Python environment
- GPU support is recommended for image feature extraction but not mandatory
- Internet access is required to download satellite images

All experiments were conducted in a controlled environment to ensure consistency and reproducibility.
## How to run the project
The project should be executed in the following order:

1. Image Acquisition
- Run the image downloading script to fetch satellite images using the provided geographic coordinates. This step prepares the raw image data required for feature extraction.
2. Preprocessing & Feature Engineering

Open and execute the preprocessing notebook to:

- Perform exploratory data analysis (EDA)
- Clean and transform tabular features
- Extract deep image embeddings using a pretrained convolutional neural network
- Optionally reduce image feature dimensionality
- Generate interpretability insights using Grad-CAM
This step produces processed datasets used for model training.

3. Model Training & Evaluation

Run the model training notebook to:

- Train baseline regression models using tabular data only
- Train multimodal models using combined tabular and image features
- Compare model performance using standard regression metrics
- Select the best-performing model
- Generate predictions on unseen test data
  
## Outputs & Reproducibility

- All intermediate datasets, extracted features, and evaluation results are saved during execution.
- Results can be reproduced by rerunning the notebooks in the specified order.
- Model comparisons are performed using consistent train–test splits and evaluation metrics.

Author

Aditi B R  
23113009

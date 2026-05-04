# Steam Game Recommender System

Collaborative filtering recommendation engine built with PySpark ALS on the Steam-200k dataset.

## Overview

This project implements a scalable game recommendation system using Apache Spark's ALS (Alternating Least Squares) algorithm. The system models user-game interactions and makes personalized game recommendations based on collaborative filtering principles.

## Key Features

- **ALS Collaborative Filtering** — Alternating Least Squares matrix factorization for implicit feedback
- **MLflow Experiment Tracking** — Automatic logging of parameters, metrics, and models
- **Hyperparameter Tuning** — CrossValidator for optimizing model performance
- **Implicit Feedback Pipeline** — Modeling user behavior as implicit signals (playtime, purchases)
- **Scalable Architecture** — PySpark enables processing large datasets efficiently

## Technologies Used

- **PySpark** — Distributed machine learning and data processing
- **MLflow** — Experiment tracking and model registry
- **Databricks** — Managed Apache Spark platform
- **Python** — Pipeline implementation and evaluation

## Dataset

- **Source**: Steam-200k dataset
- **Size**: 200,000 user-game interactions
- **File**: `steam-200k.csv`
- **Features**: user_id, game_name, playtime, purchase status

## Project Structure

```
steam-game-recommender/
├── README.md
├── .gitignore
└── notebooks/
    └── steam_recommender_system.ipynb
```

## Getting Started

### Prerequisites

- Apache Spark 3.x
- Databricks workspace or local Spark installation
- Python 3.8+
- MLflow
- Jupyter or Databricks notebook environment

### Running the Project

1. Clone this repository
2. Open `notebooks/steam_recommender_system.ipynb` in your Databricks workspace or Jupyter
3. Update the data file path to point to your `steam-200k.csv` file
4. Run all cells to train and evaluate the recommendation model

## Notebook Contents

The notebook includes:

- Setup and library configuration
- Data loading and exploratory analysis
- Data preprocessing and feature engineering
- Train-test data splitting
- ALS model configuration
- Hyperparameter tuning using CrossValidator
- Model training and evaluation
- Recommendation generation and analysis
- MLflow experiment tracking and logging

## Model Pipeline

1. **Data Preparation** — Loading and transforming raw user-game interaction data
2. **Feature Engineering** — Creating user and item embeddings
3. **Hyperparameter Tuning** — Using CrossValidator to find optimal rank, regParam, and alpha values
4. **Model Training** — Fitting the ALS model on training data
5. **Evaluation** — Assessing performance using RMSE on test data
6. **Recommendations** — Generating top-N game recommendations for users

## Results

The trained model provides:

- Personalized game recommendations for each user
- User and item latent factor representations
- Cross-validated performance metrics
- MLflow tracked experiments for reproducibility

## Configuration

Key hyperparameters:

- **Rank** — Dimension of user and item factor matrices
- **regParam** — Regularization parameter to prevent overfitting
- **alpha** — Confidence scaling for implicit feedback
- **coldStartStrategy** — Handling of users/items not in training data

## Notes

- Implicit feedback modeling treats playtime and purchases as confidence signals
- The model handles sparse user-item interaction matrices efficiently
- MLflow automatically logs all parameters, metrics, and model artifacts
- Results are reproducible through logged experiment configurations

## Author

Machine learning project demonstrating scalable recommendation systems with Spark.

## License

This project is provided as-is for educational and research purposes.

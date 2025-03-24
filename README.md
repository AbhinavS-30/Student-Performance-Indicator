# Student Performance Indicator

A complete end-to-end Machine Learning project that predicts student performance based on several academic and demographic features. Built using Scikit-Learn, Flask, and ML pipeline best practices, this project includes automated training, evaluation, deployment, and inference with a web-based UI.

## Table of Contents
- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [How It Works](#how-it-works)
- [Installation](#installation)
- [Run the App](#run-the-app)
- [Model Training and Prediction](#model-training-and-prediction)
- [Future Improvements](#future-improvements)
- [License](#license)

## Overview
This project aims to predict students’ final exam scores by analyzing various features like gender, parental education level, test preparation, and more. It includes data ingestion and transformation pipeline, model training and evaluation with logging, experiment tracking and artifact versioning, and a Flask web app for user input and predictions.

## Tech Stack
Language: Python 3.8+  
Libraries: Pandas, NumPy, Scikit-learn, Flask, Matplotlib, Seaborn  
Tools: VS Code, GitHub, MLFlow (optional), logging  
Model: Best among different choices (can be customized)

## How It Works
1. Data Collection and EDA conducted in `notebook/EDA.ipynb` using a CSV dataset containing student scores and background info.  
2. Data Pipeline includes:  
   - `data_ingestion.py` for reading and splitting the raw dataset  
   - `data_transformation.py` for encoding and scaling  
   - `model_trainer.py` for training and saving the model  
3. Training is triggered via `src/pipeline/training_pipeline.py`  
4. Prediction is handled via `predict_pipeline.py`, which loads the trained model and transformer  
5. A web app is built with Flask for interactive user input and predictions

## Installation
- Clone the repository  
- Create a virtual environment  
- Activate the environment  
- Install dependencies from `requirements.txt`  
- Create necessary folders like `artifacts` for storing model outputs

## Run the App
- Run the training pipeline using the training script  
- Start the Flask application  
- Visit `http://127.0.0.1:5000` in your browser  
- Enter student data to get a performance prediction

## Model Training and Prediction
The project uses a different models and then evaluates the best one to predict math scores. The pipeline handles:  
- Standard scaling of numerical features  
- One-hot encoding of categorical variables   
The trained model is used to serve predictions via the web interface.

## Future Improvements
- Add continuous integration and deployment with GitHub Actions  
- Integrate MLflow for experiment and model tracking  
- Dockerize the application for portability  
- Extend to classification tasks (e.g., pass/fail prediction)

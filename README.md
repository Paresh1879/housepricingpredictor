---

# Boston House Pricing Prediction - MLOps Project

## Overview

This project aims to deploy a machine learning model for predicting house prices in Boston using MLOps practices. The pipeline involves model creation, training, pickling, Dockerizing, creating a Flask web application, and deploying it to Heroku.

## Project Structure
  - **Linear Regression ML Implementation.ipynb**: Script for training and making predictions for the machine learning model.
  - **app.py**: Flask application for serving predictions.
  - **Dockerfile**: Configuration for Docker image.
- **requirements.txt**: Python dependencies.


## Setup

1. Clone this repository:

   ```bash
   git clone <repository_url>
   cd <repository_name>
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Training the Model

To train the model, run:

```bash
python src/app.py
```

The trained model will be saved in the `models/` directory.

## Dockerizing the Application

1. Build the Docker image:

   ```bash
   docker build -t boston-house-predictor .
   ```

2. Run the Docker container:

   ```bash
   docker run -p 8080:8080 boston-house-predictor
   ```

The Flask app will be accessible at `http://localhost:8080`.

## Deploy to Azure Apps Service - https://bostonhousepricingprediction.azurewebsites.net/

## Contributors

- [Paresh Natarajan](https://github.com/Paresh1879)


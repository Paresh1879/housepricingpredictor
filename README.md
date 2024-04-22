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
   docker run -p 5000:5000 boston-house-predictor
   ```

The Flask app will be accessible at `http://localhost:5000`.

## Deploying to Heroku

1. Sign up for Heroku and install the Heroku CLI.
2. Log in to Heroku:

   ```bash
   heroku login
   ```

3. Create a Heroku app:

   ```bash
   heroku create <app_name>
   ```

4. Deploy the application to Heroku:

   ```bash
   git push heroku master
   ```

## Usage

After deployment, the prediction API will be available at the Heroku app URL. Send a POST request with input features to `/predict` endpoint to get predictions.

Example using cURL:

```bash
curl -X POST -H "Content-Type: application/json" -d '{"CRIM": 0.00632, "ZN": 18.0, "INDUS": 2.31, "CHAS": 0.0, "NOX": 0.538, "RM": 6.575, "AGE": 65.2, "DIS": 4.0900, "RAD": 1.0, "TAX": 296.0, "PTRATIO": 15.3, "B": 396.90, "LSTAT": 4.98}' https://<app_name>.herokuapp.com/predict
```

## Contributors

- [Paresh Natarajan](https://github.com/Paresh1879)


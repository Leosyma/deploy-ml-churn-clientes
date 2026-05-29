# Customer Churn Prediction with Random Forest

This project is a Streamlit web application designed to predict customer churn using a trained Random Forest Machine Learning model.

The application provides an interactive interface where users can enter customer information such as age, monthly usage, satisfaction score, monthly value, plan type, and contract duration. The input data is preprocessed, scaled, and sent to a trained model that predicts whether the customer is likely to churn.

## Project Objective

The main goal of this project is to demonstrate the complete workflow of a Machine Learning solution, from model training to deployment through an interactive web application.

The application allows users to:

* Enter customer data through a Streamlit interface;
* Apply the same preprocessing steps used during model training;
* Use a trained Random Forest model to predict churn;
* Display the prediction result directly in the web app.

## Technologies Used

* Python
* Streamlit
* Pandas
* NumPy
* Scikit-learn
* Joblib
* Jupyter Notebook

## Project Structure

```text
.
├── deploy.py                  # Streamlit application for model deployment
├── Projeto2.ipynb             # Notebook used for model development and training
├── dataset.csv                # Dataset used in the project
├── dsa_modelo_final.pkl       # Trained Random Forest model
├── dsa_padronizador.pkl       # Scaler used for preprocessing
├── requirements.txt           # Project dependencies
├── LEIAME.txt                 # Original execution instructions
└── README.md                  # Project documentation
```

## How the Application Works

The application follows this workflow:

1. The trained model and scaler are loaded;
2. The user enters customer information in the Streamlit interface;
3. Categorical variables such as plan type and contract duration are converted using one-hot encoding;
4. Numerical and encoded variables are standardized using the saved scaler;
5. The processed data is passed to the trained Random Forest model;
6. The application returns whether the customer is predicted to churn.

## Input Features

The model uses the following input variables:

* Age
* Monthly usage
* Customer satisfaction score
* Monthly value
* Plan type
* Contract duration

The plan type can be:

* Basic
* Premium
* Standard

The contract duration can be:

* Short
* Medium
* Long

## Installation

Create a Conda virtual environment:

```bash
conda create --name dsadeploymlp2 python=3.13
```

Activate the environment:

```bash
conda activate dsadeploymlp2
```

Install `pip` and the project dependencies:

```bash
conda install pip
pip install -r requirements.txt
```

## Model Training

To access the notebook and train or review the model development process, run:

```bash
jupyter notebook
```

Then open the notebook file:

```text
Projeto2.ipynb
```

## Running the Application

To deploy the model with Streamlit, run:

```bash
streamlit run deploy.py
```

After running the command, Streamlit will provide a local URL where the application can be accessed in the browser.

## Prediction Output

After filling in the customer information and clicking the prediction button, the application displays the churn prediction as:

```text
Churn Predicted: Yes
```

or

```text
Churn Predicted: No
```

## Notes

* The trained model must be available as `dsa_modelo_final.pkl`.
* The scaler must be available as `dsa_padronizador.pkl`.
* The input columns used in the application must match the columns used during model training.
* This project was developed for educational purposes and demonstrates how to deploy a Machine Learning model using Streamlit.

## Author

Project developed as a practical study on Machine Learning model deployment for customer churn prediction.

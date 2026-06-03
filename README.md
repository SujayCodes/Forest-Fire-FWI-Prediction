## 🔥 Forest Fire Weather Index (FWI) Prediction System

## 📌 Project Overview
The Forest Fire Weather Index (FWI) Prediction System is a Machine Learning-based web application developed using Python Flask that predicts the Fire Weather Index (FWI) based on environmental and weather-related parameters.
The project aims to assist in forest fire risk assessment by analyzing atmospheric conditions and generating an estimated FWI score, which is an important indicator of potential fire intensity and spread.
The application provides a modern interactive web interface where users can input environmental parameters and receive real-time FWI predictions.
________________________________________
## 🚀 Features
•	Real-time Fire Weather Index prediction
•	Machine Learning-powered prediction engine
•	Interactive Flask web application
•	Data preprocessing using Standard Scaler
•	Ridge Regression model for prediction
•	Responsive modern UI
•	Dynamic result generation
•	Forest fire risk assessment support
________________________________________
## 🛠️ Tech Stack
Frontend
•	HTML5
•	CSS3
•	JavaScript
•	Jinja2 Templates
Backend
•	Python
•	Flask
Machine Learning
•	Scikit-Learn
•	NumPy
•	Pandas
Model Persistence
•	Pickle (.pkl)
________________________________________
## 📊 Dataset Information
Dataset Name
Algerian Forest Fires Dataset
Dataset Summary
The dataset contains observations collected from two regions of Algeria:
1.	Bejaia Region (Northeast Algeria)
2.	Sidi Bel-Abbes Region (Northwest Algeria)
Dataset Statistics
•	Total Records: 244
•	Bejaia Region Records: 122
•	Sidi Bel-Abbes Region Records: 122
•	Time Period: June 2012 – September 2012
•	Fire Instances: 138
•	Non-Fire Instances: 106
________________________________________
## 📥 Input Features Used
The model predicts the Fire Weather Index (FWI) using the following 9 features:
Feature	Description
Temperature	Noon temperature (°C)
RH	Relative Humidity (%)
Ws	Wind Speed (km/h)
Rain	Rainfall (mm)
FFMC	Fine Fuel Moisture Code
DMC	Duff Moisture Code
ISI	Initial Spread Index
Classes	Fire / Not Fire classification (Encoded)
Region	Region information (Encoded)
________________________________________
## 🎯 Target Variable
The target variable predicted by the model is:
FWI (Fire Weather Index)
FWI is a numerical indicator used to estimate:
•	Fire ignition probability
•	Fire intensity
•	Fire spread potential
•	Overall wildfire risk
________________________________________
## ⚙️ Data Preprocessing
Before model training, the dataset underwent preprocessing steps:
Standardization
Feature scaling was performed using:
StandardScaler()
The trained scaler was saved as:
models/scaler.pkl
This scaler is loaded during prediction to ensure incoming user inputs are transformed in the same way as the training data.
________________________________________
## 🤖 Machine Learning Model
Algorithm Used
Ridge Regression
Ridge Regression was selected to:
•	Reduce overfitting
•	Handle multicollinearity
•	Improve model generalization
•	Maintain stable predictions
The trained model was serialized using Pickle and saved as:
models/ridge.pkl
________________________________________
## 📈 Model Performance
The model achieved the following performance metrics:
Mean Absolute Error (MAE)
0.5642305340105691
R² Score
0.9842993364555513
Interpretation
•	An R² score of 98.43% indicates that the model explains nearly all variance in the Fire Weather Index.
•	A low MAE demonstrates highly accurate predictions with minimal average prediction error.
________________________________________
## 📂 Project Structure
Forest-Fire-FWI-Prediction/
│
├── application.py
│
├── models/
│   ├── ridge.pkl
│   └── scaler.pkl
│
├── templates/
│   ├── index.html
│   └── home.html
│
├── notebook/
│   ├── EDA.ipynb
│   ├── ModelTraining.ipynb
│
├── requirements.txt
│
└── README.md
________________________________________
## 🔄 Prediction Workflow
1.	User enters environmental parameters.
2.	Flask receives input data.
3.	Input data is standardized using:
o	scaler.pkl
4.	Standardized values are passed to:
o	ridge.pkl
5.	Ridge Regression predicts the Fire Weather Index.
6.	Predicted FWI value is displayed on the web interface.
________________________________________
## ▶️ Running the Project
Clone Repository
git clone <repository-url>
cd Forest-Fire-FWI-Prediction
Create Virtual Environment
python -m venv venv
Activate Virtual Environment
Windows
venv\Scripts\activate
Linux / Mac
source venv/bin/activate
Install Dependencies
pip install -r requirements.txt
Run Flask Application
python application.py
Application will be available at:
http://127.0.0.1:5000/
________________________________________
## 📚 Libraries Used
Flask
NumPy
Pandas
Scikit-Learn
Pickle
________________________________________
## 🎓 Learning Outcomes
Through this project:
•	Performed Exploratory Data Analysis (EDA)
•	Applied feature engineering techniques
•	Implemented data preprocessing pipelines
•	Trained and evaluated regression models
•	Used Ridge Regression for predictive analytics
•	Deployed a Machine Learning model using Flask
•	Built an end-to-end ML web application
________________________________________
## 👨‍💻 Author
Developed as a Machine Learning project for Forest Fire Weather Index prediction using the Algerian Forest Fires Dataset.
________________________________________
## 📄 License
This project is intended for educational, research, and learning purposes.

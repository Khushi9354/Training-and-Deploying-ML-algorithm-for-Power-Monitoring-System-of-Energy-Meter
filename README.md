# Training-and-Deploying-ML-algorithm-for-Power-Monitoring-System-of-Energy-Meter

Overview
This project focuses on building a machine learning model to classify energy meter readings based on voltage, current, and power. The goal is to accurately predict the class of an energy meter using logistic regression, a widely-used algorithm for classification tasks.

Key Steps Involved:
Data Loading:

The dataset is loaded from a CSV file containing measurements from energy meters, including voltage, current, power, and class labels.
from pandas import read_csv

url = "Energy Meter.csv"
names = ['Voltage', 'Current', 'Power', 'Class']
dataset = read_csv(url, names=names)

Data Preprocessing:

The features (Voltage, Current, Power) and target variable (Class) are extracted.
The data is split into training and validation sets, allowing for the evaluation of model performance.
Feature Normalization:

Features are standardized using StandardScaler to improve the model's performance, especially for algorithms sensitive to feature scales.
Model Training:

A logistic regression model is instantiated and trained on the training dataset.
Model Saving:

The trained model is saved to a file using Python’s pickle module for later use.
Model Evaluation:

The model is loaded from the file, and its accuracy is evaluated using the validation dataset.
Predictions can be made for new input values to classify the energy meter readings.
Results:

The model achieved a validation accuracy of approximately 99.5%, demonstrating its effectiveness in classifying the energy meter readings.
Technologies Used:
Python: The primary programming language used for data processing and modeling.
Pandas: For data manipulation and analysis.
Scikit-learn: For machine learning algorithms and model evaluation.
Matplotlib: For data visualization (if visualizations were included).
Pickle: For saving and loading the trained model.
Data Description
The dataset consists of the following columns:

Voltage: Measured voltage from the energy meter.
Current: Measured current from the energy meter.
Power: Calculated power based on voltage and current.
Class: The classification label indicating the operational state of the energy meter (e.g., Medium, NoLoad, etc.).
Conclusion
This project successfully demonstrates how to apply logistic regression for classifying energy meter data. With a high accuracy rate, the model can be useful for applications in energy management and monitoring. Future work could include experimenting with other classification algorithms, hyperparameter tuning, and exploring additional datasets for improved performance.

License
This project is licensed under the MIT License. See the LICENSE file for details.

# Customer Churn Prediction: A Deep Learning Approach

### Introduction
In today’s competitive banking environment, retaining customers is crucial. This project aims to help banks predict which customers might leave (churn) using a deep learning model. By analyzing key customer data, such as account balance and age, this tool provides insights that allow banks to take preventive action and improve customer satisfaction.

### Table of Contents
- [Key Features](#key-features)
- [Technologies Used](#technologies-used)
- [How the Data is Collected](#how-the-data-is-collected)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Model Development](#model-development)
- [MLflow Integration](#mlflow-integration)
- [Web Interface](#web-interface)
- [Installation](#installation)
- [How to Use the Application](#how-to-use-the-application)
- [Contributing](#contributing)

### Key Features
- **Churn Prediction:** Using customer details such as credit score, tenure, and salary, the model predicts whether a customer is likely to leave the bank.
- **Interactive Web Interface:** An easy-to-use web app built with Streamlit allows users to input customer information and get a prediction.
- **Data Storage:** Store predictions and user inputs in an SQLite database for easy access and future analysis.
- **Performance Tracking:** The model tracks performance metrics to continuously improve accuracy.
- **MLflow Integration:** Track the entire machine learning lifecycle, including experiments and model performance, using MLflow.

### Technologies Used
This project leverages several modern technologies:
- **Python** for data processing and model training.
- **Streamlit** to create a simple, interactive web interface for end users.
- **Pandas** for handling and analyzing customer data.
- **Keras (TensorFlow)** to build and train the deep learning model.
- **Scikit-learn** for data preprocessing and model evaluation.
- **SQLite** to store user inputs and predictions.
- **MLflow** to track and manage machine learning experiments and versions.
- **Custom Logging & Error Handling** to ensure a smooth and stable user experience.

### How the Data is Collected
The model uses a dataset that includes key customer details that can influence their decision to leave the bank, such as:
- **Credit Score**
- **Geographic Location**
- **Gender**
- **Age**
- **Tenure (years of being a customer)**
- **Account Balance**
- **Number of Products (e.g., credit cards, loans)**
- **Credit Card Ownership**
- **Active Member Status**
- **Estimated Salary**

### Data Preprocessing
To prepare the data for accurate predictions, the following preprocessing steps are applied:
- **Data Splitting:** The dataset is divided into training and test sets to ensure that the model is evaluated on data it hasn’t seen before.
- **Scaling & Encoding:** 
  - We use `RobustScaler` to scale numerical features, making the model less sensitive to outliers.
  - Categorical data, such as gender and geography, are converted into numerical form using `OneHotEncoder`.
- **Pipelines:** Scikit-learn pipelines are used to streamline the entire preprocessing workflow, ensuring all steps are applied consistently.

### Exploratory Data Analysis (EDA)
Before building the model, an in-depth analysis of the data is conducted to find patterns, trends, and relationships. Visualization tools and summary statistics are used to gain insights into customer behavior and identify key factors that lead to churn.

### Model Development
A deep learning model is developed using Keras. The model is trained to classify whether a customer is likely to churn based on their profile. This classification is then used to help the bank make informed decisions on how to retain high-risk customers.

### MLflow Integration
MLflow helps track and manage machine learning experiments. It logs parameters, metrics, and models during the training process, making it easy to monitor and compare model performance over time.
- **Tracking Experiments:** Log and monitor each experiment's parameters and results in real-time.
- **Model Registry:** Store and manage different model versions for easy deployment.
- **Visualization:** Use MLflow’s user-friendly UI to compare the performance of various models.

To start using MLflow:
1. Run the MLflow tracking server with the command:
    ```bash
    mlflow ui
    ```
2. Access the dashboard by visiting `http://localhost:5000` to monitor and visualize the experiments.

### Web Interface
The project includes an intuitive web interface built using Streamlit, designed for easy use by both technical and non-technical users. The web app allows users to:
- **Input Customer Data:** Users can enter customer details like credit score, age, and more through sliders and dropdowns.
- **Get Predictions:** After submitting the data, users instantly receive a prediction on whether the customer is likely to churn.
- **Save Data:** Users can save the input data and the corresponding predictions for future analysis in CSV format or an SQLite database.

### Installation
To run this project on your local machine, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/fdilyassine/Bank-churn-prediction-using-DL.git
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Start the Streamlit web application:
    ```bash
    streamlit run app.py
    ```

4. (Optional) If you want to use MLflow, open a new terminal and start the MLflow UI:
    ```bash
    mlflow ui
    ```

### How to Use the Application
Once everything is set up:
1. Open your web browser and go to `http://localhost:8501` to access the app.
2. Enter the customer details like age, credit score, and salary.
3. Click the "Predict" button to receive a prediction on whether the customer is at risk of churning.
4. You can also choose to save the customer data and prediction results for future use in a CSV file or database.

### Contributing
Contributions are welcome! If you have any suggestions or improvements, feel free to fork the repository and submit a pull request. You can also open issues to discuss potential enhancements or bug fixes.

We look forward to your feedback and collaboration!

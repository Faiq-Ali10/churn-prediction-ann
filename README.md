# Telco Customer Churn Prediction

This project involves predicting customer churn for a telecommunications company using a dataset from Kaggle. The goal is to explore, preprocess, and model the data using a deep learning approach (Artificial Neural Network, ANN). The project includes data preprocessing techniques such as scaling and oversampling (SMOTE) to improve model performance.

## Dataset

The dataset is sourced from Kaggle and contains information about customers, including details such as tenure, services, and account information. The target variable is whether a customer churned (left the company) or not.

### Dataset Link:
[Kaggle Telco Customer Churn Dataset](https://www.kaggle.com/blastchar/telco-customer-churn)

## Project Overview

The project is structured as follows:

1. **Data Exploration**: Understanding the dataset, visualizing key features, and inspecting missing values.
2. **Data Preprocessing**:
    - Handling missing values
    - Encoding categorical variables
    - Scaling numerical features using MinMax Scaling
    - Applying SMOTE for balancing the dataset (as it contains class imbalance)
3. **Modeling**:
    - Building an Artificial Neural Network (ANN) for binary classification (predicting customer churn).
    - Model Evaluation using accuracy and other classification metrics.
4. **Results**: Reporting the model’s performance on both training and test data.

## Steps Performed

### 1. Data Exploration
We began by exploring the dataset to understand the structure and relationships between variables. Key steps included:
- Checking for missing values
- Analyzing the distribution of the target variable (Churn)
- Visualizing key relationships between features

### 2. Data Preprocessing
The preprocessing steps involved:
- **Missing Value Handling**: Replaced missing values with appropriate imputation strategies.
- **Feature Encoding**: Converted categorical variables into numerical representations.
- **Feature Scaling**: Applied MinMax scaling to normalize numerical features.
- **Handling Class Imbalance**: Used SMOTE (Synthetic Minority Over-sampling Technique) to generate synthetic samples of the minority class (churned customers).

### 3. Model Building (Artificial Neural Network)
The model used is a Sequential neural network built with Keras:
- Input layer with 23 features.
- Hidden layers with 15 units each and ReLU activation functions.
- Output layer with 1 unit and sigmoid activation function for binary classification.

The model was compiled with:
- **Adam optimizer**
- **Binary cross-entropy loss function**
- **Accuracy metric** to monitor performance during training

The model was trained for 20 epochs with a batch size of 32 on the preprocessed and balanced dataset.

### 4. Evaluation and Results
The model was evaluated on the test set, and performance metrics such as accuracy, precision, recall, and F1-score were calculated.

## Results

The model achieved the following results:
- **Train Accuracy**: 81%
- **Test Accuracy**: 76%

### Further Steps
- Experiment with hyperparameter tuning (e.g., learning rate, number of epochs, batch size).
- Test with different architectures (e.g., more layers, different activation functions).
- Try other models like Random Forest or XGBoost to compare performance.

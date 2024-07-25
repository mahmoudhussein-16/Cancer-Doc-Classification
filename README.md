## Description

This project focuses on classifying biomedical text documents related to cancer into three categories: Thyroid Cancer, Colon Cancer, and Lung Cancer. The dataset includes abstracts and full papers, specifically targeting research papers longer than six pages. The total number of publications in the dataset is 7569, distributed as follows:

- Colon Cancer: 2579 samples
- Lung Cancer: 2180 samples
- Thyroid Cancer: 2810 samples

## Function

The primary function of this project is to implement various machine learning models to classify cancer-related research documents into their respective categories. The steps involved in this project include:

1. **Data Collection**: Using the `opendatasets` library to fetch the required dataset.
2. **Data Preprocessing**: Tokenizing text, removing stop words, stemming, and vectorizing the text data using TF-IDF.
3. **Exploratory Data Analysis (EDA)**: Visualizing the data distribution and understanding the features.
4. **Model Training**: Training multiple machine learning models, such as Naive Bayes, Random Forest, SVM, Logistic Regression, and more.
5. **Model Evaluation**: Evaluating the performance of these models using accuracy score, confusion matrix, and classification report.

## Installation & Setup

To set up the project, the necessary libraries can be installed using the following command:

bash

Copy code

`pip install opendatasets pandas numpy matplotlib seaborn nltk wordcloud scikit-learn flask joblib`

## Usage

The project is implemented in a Jupyter Notebook, and the steps can be followed to replicate the classification process. The notebook includes code cells for data preprocessing, model training, and evaluation.

## Deployment

This project includes a deployment of the trained model using a Flask API. The Flask API provides an endpoint for making predictions on new data.

### Flask API Setup

1. **Install Flask**: Ensure Flask and other required libraries are installed:
    
    bash
    
    Copy code
    
    `pip install flask joblib`
    
2. **Run the Flask App**: The `app.py` file contains the code for the Flask API. You can run the API using the following command:
    
    bash
    
    Copy code
    
    `python app.py`
    
3. **API Endpoint**: The API provides a `/predict` endpoint that accepts POST requests with the input data in JSON format. The input data should be a list of features to be classified. Example request format:
    
    json
    
    Copy code
    
    `{     "input": [[feature1, feature2, ..., featureN]] }`
    
4. **Response**: The API returns the predictions in JSON format.

## Conclusion

This project provides a comprehensive approach to classifying biomedical text documents related to cancer, utilizing various machine learning techniques to achieve accurate classification results. Additionally, the deployment using a Flask API enables easy integration with other applications for making predictions on new data.

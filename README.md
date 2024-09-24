
# Alphabet Soup Charity Funding Predictor

## Project Overview

This project aims to build and compare two machine learning models: a Neural Network and a Random Forest classifier. The goal is to predict whether a charity funding applicant will be successful based on their application data. We used data provided by Alphabet Soup, which contains over 34,000 records of organizations that have received funding in the past.

## Models Used
1. **Deep Neural Network (DNN)**:
   - Utilized to capture complex patterns in the data.
   - Accuracy: 72.71%
   - Loss: 0.5660
   
2. **Random Forest Classifier**:
   - A traditional machine learning model used for comparison.
   - Accuracy: 71.0%

Based on the results, the Neural Network model slightly outperformed the Random Forest model.

## Dataset
The dataset includes the following features:
- **Application Type**: Type of application submitted.
- **Affiliation**: Sector of the applicant's organization.
- **Classification**: Government classification of the organization.
- **Income Amount**: Income level of the applicant.
- **Special Considerations**: Whether special considerations were requested.
- **Funding Amount Requested**: Amount of funding requested.

The target variable is `IS_SUCCESSFUL`, which indicates whether the funding was used effectively by the applicant.

## Project Workflow

### 1. Data Preprocessing:
- Dropped unnecessary columns such as `EIN` and `NAME`.
- Encoded categorical variables using `pd.get_dummies`.
- Grouped rare categorical values into a new category called 'Other' based on a chosen cutoff point.
- Scaled the data using `StandardScaler`.

### 2. Model Training:
- **Neural Network**: Two hidden layers were used to capture complex patterns, with ReLU activation for the hidden layers and sigmoid activation for the output layer.
- **Model Optimization**: Various techniques were applied, including adjusting the number of neurons, layers, and epochs to improve performance. Despite optimization attempts, the accuracy remained similar.
- **Random Forest**: A Random Forest model with 130 estimators was trained for comparison.

### 3. Model Evaluation:
- The models were evaluated on test data. The Neural Network performed slightly better with a 72.71% accuracy, while the Random Forest achieved 71.0% accuracy.
- The Random Forest model was used as an alternative to the Neural Network. Although the Random Forest performed slightly worse, it may be more suitable for simpler datasets or when faster training time is needed.

## Installation and Requirements

To run the project, you need to install the following libraries:
- **TensorFlow**
- **Scikit-learn**
- **Pandas**

To install the libraries, run the following command:

```bash
pip install tensorflow scikit-learn pandas
```

## Files Included

- **AlphabetSoup_DeepLearning_RF_Comparison.ipynb**: Jupyter notebook containing all the code for data preprocessing, model training, and evaluation.
- **AlphabetSoupCharity.keras**: The saved Neural Network model in Keras format.
- **AlphabetSoupCharity.h5**: The saved Neural Network model in HDF5 format.

## Resources

- [TensorFlow Documentation](https://www.tensorflow.org/learn)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)


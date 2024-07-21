# financial_classification_model
## Project Overview
This project utilizes multiple different machine learning techniques to predict binary classification of loan status.

## Installation
The notebooks in this repository should be ran in Google Colab to ensure data is imported correctly.

## Description of Files
- 'financial_classification_model.h5' - the model exported from 'financial_classification_model.ipynb'
- 'financial_classification_model.ipynb' - the notebook used for data preprocessing and model creation
- 'optimization.ipynb' - the notebook used for two optimization attempts
- 'optimization_2.ipynb' - a third optimization attempt

## Data
- The dataset used was in CSV format and had the following columns:
    - Target Variable: 'IS_SUCCESSFUL'
    - Features: 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', 'ASK_AMT'
    - Dropped Columns from original dataset: 'EIN' and 'NAME' because they were labels unneeded for model development

## Preprocessing:
- Preprocessing was slightly varied accross different notebooks for optimization of the models and generally included:
    - Dropping labels
    - Scaling continuous variables
    - Encoding categorical variables
    - Splitting data into Train and Test Groups

## Results and Recommendations
- After several attempts working with the Keras Sequential model, with varied optimization techniques employed, the peak accuracy observed was 73%.
- This suggests that a recomendation for a different model would be advantageous,
- Models from sklearn library such as KNN, Logistic Regression, and Gradient Boosting may be able to handle the prediction task more accurately
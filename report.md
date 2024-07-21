# Financial Classification Model

## 1. Overview:
    
    The purpose of this project is to create a neural network model that can, with at least 75% accuracy, predict a loan's chances of approval.

## 2. Results:
    
    * Data Preprocessing
        - Target Variable: 'IS_SUCCESSFUL'
        - Features: 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', 'ASK_AMT'
        - Dropped Columns from original dataset: 'EIN' and 'NAME' because they were labels unneeded for model development
    
    * Compiling, Training, and Evaluating the Model
        - The first neural network consisted of two hidden layers with 'relu' activation functions with an output layer having the 'sigmoid' activation function. 
        - Respectively there were 80, 30, in the hidden layers with a single neuron in the output layer.
        - This model reached an accuracy score of 72% after 15 Epochs of training, falling 3% short of the target goal.
        - Many attempts were made in 'optimization.ipynb' and 'optimization_2.ipynb' to increase the accuracy score.
            * The approach to the two attempts in 'optimization.ipynb' utilized the same preprocessing as the original model and adjusted the model's architecture and amount of Epochs for training.
            * The increase seen by these efforts was nominal. A 1% gain in accuracy was observed and could possibly be interpreted as a result of overfitting.
            * The approach in 'optimization_2.ipynb' utilized different preprocessing techniques as well as additional training optimizations.
                - Preprocessing utilized logging continuous values to handle skew
                - Training utilized EarlyStopping and ReduceLROnPlateau to ensure optimum learning rates
            * The overall outcome of this attempt did not realize any meaningful gaines to accuracy

## 3. Summary:
    
    * Overall, the best accuracy observed in the neural network model was 73%
    * Small changes were seen in the multiple optimization attempts
    * This suggests a different model may be better equipped to handle the classification problem such as KNeighbors, Logistic Regression, Gradient Boosting, etc.. from sklearn.
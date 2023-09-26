# Deep Learning Challenge: Alphabet Soup
![Modern neural network Instagram Story ](https://github.com/mehpree/deep-learning-challenge/assets/131678606/18ee5830-9956-4057-a34e-cf116d550be5)

## Overview
In this project, I was tasked with creating a binary classification model to predict the success of organizations funded by Alphabet Soup, a nonprofit foundation. The goal was to determine which applicants have the best chance of success in their ventures based on provided features.

## Step 1: Data Preprocessing
### Data Loading
- I began by loading the dataset from the "charity_data.csv" file into a Pandas DataFrame.

### Identifying Target and Features
- The target variable for the model was identified as the "IS_SUCCESSFUL" column, which indicates whether the organization was successful after receiving funding.
- Feature variables for the model were selected based on their relevance to the prediction task.

### Dropping Unnecessary Columns
- I removed the "EIN" and "NAME" columns as they were identifiers and did not contribute to prediction.

### Checking Unique Values
- For each column, I calculated the number of unique values to understand the dataset's diversity.
- Columns with more than 10 unique values were further analyzed.

### Binning Rare Categories
- Based on my analysis, I grouped categories with very few data points into a new category called "Other."

### Encoding Categorical Variables
- I used one-hot encoding (`pd.get_dummies()`) to convert categorical variables into a numerical format.

### Train-Test Split and Scaling
- The data was split into training and testing datasets using the `train_test_split` function.
- Feature scaling was performed using `StandardScaler` to ensure consistent scales for all features.

## Step 2: Building and Evaluating the Model
### Model Creation
- I designed a neural network model using TensorFlow and Keras.
- The model included input layers, hidden layers, and an output layer.
- Appropriate activation functions were selected for each layer.

### Compiling and Training
- I compiled the model, specifying the loss function, optimizer, and metrics.
- The model was trained on the training data, with a defined number of epochs and batch size.
- A callback was implemented to save model weights every five epochs.

### Model Evaluation
- The trained model was evaluated using the test data to calculate loss and accuracy.

### Saving the Model
- The trained model was saved to an HDF5 file named "AlphabetSoupCharity.h5."

## Step 3: Model Optimization
- I attempted various optimization techniques to achieve a target predictive accuracy higher than 75%.
- Optimization strategies included data preprocessing modifications, adjusting the neural network architecture, and modifying hyperparameters.

This concludes the Deep Learning Challenge for Alphabet Soup, where I successfully built, trained, and optimized a neural network model to predict the success of funded organizations. The model's performance met the target accuracy, demonstrating its suitability for the classification problem.

## References
IRS. [Tax Exempt Organization Search Bulk Data Downloads](https://www.irs.gov)

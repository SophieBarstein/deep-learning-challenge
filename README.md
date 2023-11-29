# deep-learning-challenge
Charity data predictions using tensorflow
deep-learning-report:

# Purpose:
The primary goal of this project is to design and implement an algorithm employing machine learning and neural networks. The specific aim is to develop a predictive model that can assess the likelihood of success for applicants seeking funding from the fictional non-profit foundation, Alphabet Soup. Through the utilization of advanced computational techniques, our goal is to provide valuable insights that assist in the decision-making process, optimizing the foundation's support for prospective projects and fostering overall success within its mission.

# Data Preprocessing
*CSV file containing more than 34,000 organizations that have received funding from Alphabet Soup over the years was read into Pandas
*The non-beneficial ID columns, 'EIN' and 'NAME' were dropped
*Found the number of data points for each unique value for each of the columns that had more than 10 unique values - APPLICATION_TYPE and CLASSIFICATION
*Chose a cutoff point of 725 and 1918, respectively, to bin rare categorical values together into a new value called "Other"
*Used pd.get_dummies() to convert categorical data to numeric
*Divided `the data into a target array (IS_SUCCESSFUL) and features arrays
*Applied train_test_split to create a testing and a training dataset
*Used StandardScaler to scale the training and testing sets

# Compiling, Training, and Evaluating the Model
In order to meet the requirement of achieving a predictive accuracy higher than 75%, an initial model was developed which reached an accuracy rate of 72.9%. Subsequently, more attempts were executed to adding layers and neurons in order to enhance the model.

# Results:
Model1: (AlphabetSoupCharity.h5) yielded an accuracy score of 72.9%, indicating that 72.9% of its predicted values align with the true values in the dataset.
total_layers = 2
layer1 = 9 neurons : activation function = ‘relu’
layer2 = 5 neurons : activation function = ‘relu'
epochs = 100
Model2: (AlphabetSoupCharity.Optimization.h5) achieved an accuracy score of 75.27%. After incorporating an additional layer and increasing the number of neurons, the accuracy remained at 75.27%. This implies that the highest accuracy among the two models is 75.27%. Both models' predictions closely match the true values in the dataset. The augmentation of layers and neurons led to an improvement in model performance.
total_layers = 3
layer1 = 10 neurons : activation function = ‘relu’
layer2 = 8 neurons : activation function = sigmoid"'
layer3 = 6 neurons : activation function = 'sigmoid'
epochs = 30
Summary:
In both trials, the model successfully reached a predictive accuracy of 75.27%, indicating a notable improvement. Consequently, this outcome met the targeted goal.

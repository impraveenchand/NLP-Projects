# NLP Projects

## Project-1
### Multi-Class Text Classification to Predict Happiness Source (Using ML Algorithms):
 
Smile is a corpus of more than 100,000 happy moments crowd-sourced via Amazon's Mechanical Turk

Each worker is given the following task: What made you happy today? Reflect on the past 24 hours and recall three actual events that happened to you that made you happy. Write down your happy moments a complete sentence. (Write three such moments.)

The goal of the corpus is to advance the understanding of the causes of happiness through text-based reflection.

## Based on the happy moment statement you have to predict the category of happiness, i.e the source of happiness which is typically either of the following: 'bonding: 'achievement', 'affection', 'leisure', 'enjoy the moment', 'nature', 'exercise'

### Approach 1:
## Create a Pipeline to Predict Happiness Source.
1. Import the required libraries
2. Load the DataSet into Pandas Dataframe
3. Check for missing values
4. Check the Label column and find out the count of the classes
5. Split the data into train & test sets
6. Text Preprocessing using Scikit-learn's library
7. Build a pipeline to vectorize the text data, then train and fit a model. After that evaluate the performance of the model on the test data based on weighted Avg F1_score-Metric.
8. Select the model which has high F1_score and generalizes well on the test data.
9. Predict the Category of Happiness on Unseen data(hm_test).

## Observations:
Linear Support Vector classifier model has the highest f1_score(93 %) out of all the models. And Naive Bayes classifier has the least f1_score(66%).So, we have to select Support Vector as the best model and by using it we have to Predict the Category of Happiness on Unseen data.

### Approach 2:
### Multi-Class Text Classification to Predict Happiness Source (Using DL Recurrent Neural Networks):
## Create a seperate Pipeline for neural network approach:
1. Import the required libraries
2. Clean the text data
3. Tokenize and find out the count of unique words
4. Convert text to sequences and padding
5. Split the data into train & test sets
6. Build a sequencial model and complie it
7. Fit the model on train data
8. Evaluate the model on test data

## Observation:
By using LSTM as the neurons for the hidden layers, I built the deep neural network model and got 88.7% accuracy on the test data.The LinearSVC model is performing better than the LSTMs model on the test data. So, the best model to predict the happiness source is LinearSVC.




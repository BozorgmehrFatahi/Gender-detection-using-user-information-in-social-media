# Gender-detection-using-user-information-in-social-media
# NLP Gender Classification Model
This repository contains code for a Natural Language Processing (NLP) gender classification model using Python. The model is built using the RandomForestClassifier algorithm and utilizes the TfidfVectorizer for text feature extraction.

## Project subject
Today, social networks have wide applications. Its first use is entertainment and free time. But from another point of view, social networks can be used to find behavioral patterns. For example, by analyzing the opinions of social network users, we can find the weaknesses of our business
Gender is one of the influencing parameters in users' behavior. Faced with an issue, women will mostly react in one way and men in another way!
Now, in this project, we are going to predict their gender with the information provided by Datak from Twitter and Instagram users.

## Dataset
The training data is loaded from a CSV file located at '../data/train_data.csv'. The dataset contains features such as 'fullname', 'username', 'biography', and the target variable 'gender'.

## Data Preprocessing
- Text data from 'fullname', 'username', and 'biography' columns is combined and transformed using TfidfVectorizer.
- The target variable 'gender' is mapped to numerical values ('man': 0, 'woman': 1).

## Model Training
- A GridSearchCV is used to find the best hyperparameters for the RandomForestClassifier.
- The model is trained on the encoded text data and predicts the gender based on the text features.
- Feature columns 'fullname', 'username', and 'biography' are dropped from the training data.
- The dataset is split into training and validation sets using train_test_split.

## Model Evaluation
- The model's performance is evaluated using classification reports and F1 scores on both the training and validation sets.
- The best hyperparameters found by GridSearchCV are used to train the final model.
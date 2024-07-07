# Mail Spam Detection

This repository contains a project to detect spam mail using a neural network built with PyTorch. The project involves preprocessing the data, vectorizing the text, building a neural network, and training it to classify mails as spam or ham (not spam).

## Project Structure

- `MailSpamDetection.ipynb`: Jupyter notebook containing the entire workflow from data loading to model training and evaluation.
- `README.md`: Documentation for the project.

## Dataset

The dataset contains the following columns:

- `label`: Indicates whether the mail is spam or ham.
- `text`: The content of the mail.

## Preprocessing

The preprocessing steps include:

1. Loading the dataset from a URL.
2. Dropping unnecessary columns.
3. Checking for and handling any missing values.
4. Plotting the distribution of spam and ham mail.
5. Cleaning the text by removing non-alphabetic characters, converting to lowercase, removing stopwords, and lemmatizing the words.
6. Replacing the labels with numeric values (spam: 1, ham: 0).

## Model

The neural network is built using PyTorch and has the following structure:

- Input layer with 7048 features (number of unique words after vectorization)
- Two hidden layers with 64 units each and ReLU activation
- Output layer with 1 unit for binary classification

## Training

The training process involves:

1. Splitting the data into training and testing sets.
2. Training the model for 10 epochs.
3. Recording the training and testing losses and accuracies for each epoch.

## Evaluation

The model's performance is evaluated by plotting the training and testing losses and accuracies over the epochs.

## Dependencies

- pandas
- chardet
- requests
- matplotlib
- nltk
- scikit-learn
- torch
- torchinfo

## Results

The training and testing losses and accuracies are plotted to show the model's performance over the epochs. The model can also be used to predict whether a given mail is spam or ham.

## Conclusion

This project demonstrates a basic approach to detecting spam mails using a neural network in PyTorch. Further improvements can be made by tuning the model architecture, experimenting with different loss functions and optimizers, and using more advanced preprocessing techniques.

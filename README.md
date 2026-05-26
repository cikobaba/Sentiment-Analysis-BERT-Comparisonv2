# Sentiment Analysis BERT Comparison

This repository contains the source code used in my bachelor thesis. The project focuses on sentiment analysis of Shopify customer reviews using transformer-based language models.

The main aim of the study is to compare BERT, RoBERTa, and DistilBERT on the same small and imbalanced e-commerce review dataset. The models are evaluated using both classification performance and practical efficiency measures.

## Project Overview

Customer reviews are important for e-commerce businesses because they show customer opinions about products and services. In this project, Natural Language Processing techniques are used to classify Shopify customer reviews into three sentiment categories:

- Negative
- Neutral
- Positive

The sentiment labels were created from 1–5 star ratings:

- 1–2 stars: Negative
- 3 stars: Neutral
- 4–5 stars: Positive

## Models Used

The following transformer-based models were compared:

- BERT
- RoBERTa
- DistilBERT

The same dataset and similar training structure were used for each model in order to make the comparison fair.

## Dataset

The dataset consists of Shopify customer reviews. The review text was used as the main input for the models. The rating values were used to create sentiment labels.

The dataset is small and imbalanced, which reflects a realistic low-data situation for small e-commerce businesses.

## Main Processing Steps

The code includes the following steps:

- Loading the Shopify review dataset
- Selecting the review text and rating columns
- Removing empty reviews
- Removing duplicate reviews
- Translating non-English reviews into English
- Converting 1–5 star ratings into sentiment labels
- Splitting the dataset into training, validation, and test sets
- Fine-tuning BERT, RoBERTa, and DistilBERT
- Evaluating model performance
- Measuring inference time and GPU memory usage

## Evaluation Metrics

The models were evaluated using the following classification metrics:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- Prediction distribution

In addition, practical efficiency was evaluated using:

- Inference time
- GPU memory usage

These measures were included because small businesses may need models that are not only accurate, but also faster and lighter to use.

## Original Code Structure

The implementation was adapted from the following original Colab notebook:

[Fine-tuning BERT and friends for multi-label text classification](https://colab.research.google.com/github/NielsRogge/Transformers-Tutorials/blob/master/BERT/Fine_tuning_BERT_(and_friends)_for_multi_label_text_classification.ipynb)

The original notebook structure was modified for single-label sentiment classification of Shopify customer reviews.

## Main Changes Made

The original notebook was adapted with the following changes:

- Changed the task from multi-label classification to single-label sentiment classification
- Added custom Shopify review dataset loading
- Added review text cleaning steps
- Added duplicate and empty review removal
- Added translation of non-English reviews into English
- Added rating-based sentiment labeling
- Adapted the code for BERT, RoBERTa, and DistilBERT
- Added confusion matrix and prediction distribution analysis
- Added inference time measurement
- Added GPU memory usage measurement

## Purpose of the Repository

This repository is created to provide the source code for the thesis experiment and to make the implementation more transparent and reproducible.

## Notes

This project was developed for academic purposes. The results may be affected by the small and imbalanced structure of the dataset.

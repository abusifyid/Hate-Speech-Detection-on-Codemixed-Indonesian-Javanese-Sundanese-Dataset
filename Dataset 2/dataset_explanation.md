
# Hate Speech Detection Dataset (Code-Mixed Javanese-Indonesian and Sundanese-Indonesian)

## Overview

This dataset is designed for hate speech detection in code-mixed Javanese-Indonesian and Sundanese-Indonesian languages. The dataset was expanded using data augmentation techniques to improve the robustness and performance of machine learning models. The original data consists of tweets that have been labeled as either hate speech or not hate speech, and it was sourced from a previous study focusing on hate speech detection in code-mixed languages.

## Augmentation Strategies

To enhance the dataset, two data augmentation strategies were applied: **Paraphrasing** and **Aggressive Text Transformation**. These strategies were implemented using the GPT-4o model from OpenAI via its API, generating augmented data based on specialized prompts for Javanese-Indonesian and Sundanese-Indonesian texts.

### 1. Paraphrasing Strategy

The paraphrasing approach aims to generate alternate versions of the original tweets while maintaining the same context and meaning. This method introduces slight variations to the text, which helps in maintaining the coherence and relevance of the data. 

- **Goal**: To keep the augmented data contextually similar to the original dataset.
- **Drawback**: May not introduce enough diversity, limiting the model’s generalization ability.
- **Output**: Each input tweet is paraphrased into five different versions.

### 2. Aggressive Transformation Strategy

This strategy focuses on creating more diverse transformations of the original tweets while maintaining the same abusiveness level. The goal is to broaden the dataset’s scope, making it more versatile and capable of covering a wider range of contexts.

- **Goal**: To introduce more substantial differences while preserving the abusive nature of the tweets.
- **Risk**: Some examples might deviate too much from the original context, potentially introducing inconsistencies.
- **Output**: Each input tweet generates three transformed versions.

## Dataset Files

The dataset consists of the following files:

- **jawa-train.csv**: The original training set for the Javanese-Indonesian code-mixed language.
- **jawa-test.csv**: The test set for the Javanese-Indonesian code-mixed language.
- **jawa-train-augmented-paraphrasing.csv**: The training set augmented using the paraphrasing strategy for the Javanese-Indonesian data.
- **jawa-train-augmented-aggressive-transformation.csv**: The training set augmented using the aggressive transformation strategy for the Javanese-Indonesian data.
- **sunda-train.csv**: The original training set for the Sundanese-Indonesian code-mixed language.
- **sunda-test.csv**: The test set for the Sundanese-Indonesian code-mixed language.
- **sunda-train-augmented-paraphrasing.csv**: The training set augmented using the paraphrasing strategy for the Sundanese-Indonesian data.
- **sunda-train-augmented-aggressive-transformation.csv**: The training set augmented using the aggressive transformation strategy for the Sundanese-Indonesian data.

## Purpose

The augmented data in this dataset was created to improve the performance of machine learning models for hate speech detection in code-mixed languages. The diversity introduced by both the paraphrasing and aggressive transformation strategies is intended to help the models generalize better across different domains and contexts.

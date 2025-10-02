
# Disaster Tweet Classification - NLP Project
## Project Overview
This project tackles the Natural Language Processing with Disaster Tweets Kaggle competition. The goal is to build a machine learning model that can classify whether a tweet is about a real disaster or not, distinguishing literal disaster reports from metaphorical language.

## Problem Statement
Twitter (X) has become an important communication channel during emergencies. However, it's challenging for machines to distinguish between tweets about actual disasters and those using disaster-related words metaphorically. For example:

Real Disaster: "Forest fire near LA, evacuation orders issued"

Not Disaster: "My new album is fire 🔥 #ablaze"

## Dataset
The dataset contains 10,000 hand-classified tweets with the following structure:

Column	Description
id	Unique identifier for each tweet
text	The content of the tweet
location	Location user was tweeting from (may be blank)
keyword	Particular keyword from tweet (may be blank)
target	1 for real disaster, 0 for not disaster
Target Distribution:

🟢 Non-Disaster Tweets: ~57%

🔴 Disaster Tweets: ~43%

# Technical Implementation
## Preprocessing Pipeline
Text Cleaning: URL removal, mention/hashtag handling, punctuation removal

Tokenization: Word tokenization with NLTK

Normalization: Lowercasing, stopword removal, lemmatization

Advanced Processing: POS tagging for contextual understanding

## Feature Engineering
Text Features:

1. TF-IDF vectors with n-grams (1,2)
2 Custom vocabulary based on disaster terminology
3. Structural Features:

- Text length, word count, character count
- Lexical diversity and complexity metrics
- Social media patterns (hashtags, mentions, URLs)

###Domain-Specific Features:
- Disaster keyword counts
- Urgency indicators
- Sentiment analysis scores
- Emotional language markers

## Models Implemented
Model	Description	Key Features
Logistic Regression + TF-IDF	Strong baseline model	Text features only
Naive Bayes + TF-IDF	Fast probabilistic model	Efficient text classification
Combined Features + LR	Advanced ensemble	Text + engineered features
Random Forest	Tree-based ensemble	Numeric feature patterns

 ##Model Performance
Model	Validation F1 Score	Key Strengths
Logistic Regression (TF-IDF)	~0.78-0.82	Interpretable, fast
Combined Features + LR	~0.80-0.84	Best overall performance
Ensemble Methods	~0.82-0.85	Most robust


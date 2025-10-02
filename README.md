
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
1. Logistic Regression + TF-IDF	Strong baseline model	Text features only
2. Naive Bayes + TF-IDF	Fast probabilistic model	Efficient text classification
3. Combined Features + LR	Advanced ensemble	Text + engineered features
4. Random Forest	Tree-based ensemble	Numeric feature patterns

 ##Model Performance
1. Model	Validation F1 Score	Key Strengths
2. Logistic Regression (TF-IDF)	~0.78-0.82	Interpretable, fast
3. Combined Features + LR	~0.80-0.84	Best overall performance
4. Ensemble Methods	~0.82-0.85	Most robust

## Key Features & Innovations
### Advanced Text Analysis
- Word Cloud Visualization: Compare disaster vs non-disaster vocabulary
- Distinctive Word Analysis: Identify class-specific terminology
- Structural Pattern Recognition: Analyze tweet composition differences

## Sophisticated Feature Engineering
- Multi-level Features: 20+ engineered features capturing different aspects
- Domain Knowledge Integration: Disaster-specific keyword libraries
- Sentiment Integration: Emotional vs factual language differentiation

## Ensemble Strategies
- Weighted Voting: Performance-based model weighting
- Probability Calibration: Confidence-based prediction thresholds
- Multiple Submission Strategies: A/B testing different approaches

## Results & Insights
###Performance Highlights
- Best Single Model: Combined Features + Logistic Regression
- Ensemble Improvement: +2-3% over best single model
- Key Success Factors: Feature engineering + model combination

## Important Findings
- Structural features complement text content effectively
- Disaster-specific keywords are strong predictors
- Ensemble methods consistently outperform single models
- Feature interpretability helps understand model decisions

## Acknowledgments
1. Kaggle for hosting the competition and providing the dataset
2. Figure-Eight for originally creating and sharing the dataset
3. Scikit-learn and NLTK communities for excellent NLP tools


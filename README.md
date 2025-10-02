
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

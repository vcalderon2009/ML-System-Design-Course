# Module 0 - Homework - Twitter Sentiment Analysis

This week, we covered an **Intro to NLP**. It introduced concepts for how
to analyze a corpus of text; use `spaCY` for running an NLP pipeline; and
how NLP works.

## Problem statement

Airline industry had a very hard time post-covid to sustain their business
due to a long hault. It is very important for them to make sure they exceed
customer expectations. The best way to evaluate performance is customer
feedback. You are given a dataset of *airline tweets* from real customers.

A sentiment analysis job about the problems of each major U.S. airline.
Twitter data was scraped from *February of 2015* and contributors
were asked to first classify *positive*, *negative*, and *neutral* tweents,
followed by categorizing *negative reasons* (e.g. "late flight", or
"rude service").

You will use the text column and sentiment column to create a classification
model that classifies a given tween into one of the 3 classes:

- Positive
- Negative
- Neutral

## Understanding the dataset

Dataset contains many columns, out of which below are most important ones:

1. `airline_sentiment` : Defines the sentiment of the tweet
2. `negative_reason` : Reason for the negative feedback (if negative).
3. `Text` : Tweet text content
4. `tweet_location` : Location, from which the tweet was posted.

## Steps to perform

1. Load dataset: [link][datasetURL]
2. Clean, preprocess data and EDA.
3. Vectorise columns that contain text.
4. Run classification model to classify - *positive*, *negative*, or *neutral*.
5. Evaluate model.

## Resources

- [Jupyter Notebook Assignment][jupyterNotebook]
- [Kaggle][kaggleURL]
- [spaCy][spacyURL]
- [NLTK][nltkURL]



[jupyterNotebook]: https://github.com/hamzafarooq/maven-mlsystem-design-cohort-1/blob/main/Module-0/airline_tweet_sentiment.ipynb

[datasetURL]: https://www.kaggle.com/datasets/crowdflower/twitter-airline-sentiment

[spacyURL]: https://spacy.io/

[kaggleURL]: https://www.kaggle.com/

[nltkURL]: https://www.nltk.org/

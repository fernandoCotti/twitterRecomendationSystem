# Social Network Link Prediction with Content-Based Features

Link prediction means predicting future interactions between entities in a network. In a social network, that could be friendships, interactions or associations between users.
This project predicts whether a pair of Twitter users will interact, based on how similar the content of their tweets is.

## What the notebook does

**1.** **Data loading:** Loads tweets, the candidate user pairs to predict, and the ground-truth labels from CSV files.<br/>
**2.** **Graph construction:** Builds a directed interaction graph with NetworkX. Users are nodes, mentions are edges, and retweet counts are edge weights.<br/>
**3.** **Content-based feature:** For each candidate pair, it computes the word-overlap (Jaccard) similarity between the two users' most recent tweets. Features for a random sample of 500 pairs are computed in parallel with joblib.<br/>
**4.** **Model training and evaluation:** Splits the sample 80/20, trains a Random Forest classifier, and evaluates it with precision, recall and nDCG@5/10/20.

## Tech stack

Python, pandas, NetworkX, scikit-learn, joblib, Google Colab

## Possible extensions

These are not implemented yet:
- Network-topology features computed from the graph (common neighbours, Jaccard coefficient, Adamic–Adar).
- Richer text similarity (TF-IDF, word embeddings) and using a user's whole tweet history instead of only the latest tweet.
- Training on the full candidate set instead of a 500-pair sample, ranking pairs by predicted probability, and reporting/visualising the predicted links.

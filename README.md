# Social Network Link Prediction with Content-Based Features

Content-based features are extracted from the text of tweets shared by users. 
These features capture the similarity between the content of tweets shared by pairs of users, using techniques such as TF-IDF, word embeddings, or simple word overlap.
This project aims to develop a link prediction system for social networks by combining both network topology and content-based features. 
Link prediction involves predicting future interactions between entities in a network. 
Within social networks, this could include predicting friendships, interactions, or associations between users.

This project was designed based on the following steps:

**1.** **Data Loading and Exploration:** Loading data from CSV files containing user interactions and tweet data.<br/>
**2.** **Graph Construction:** Building a directed graph representing user interactions based on the data provided, with users as nodes and interactions as edges.<br/>
**3.** **Feature Engineering:** Generating features for link prediction, including both network-based features (e.g., common neighbors, Jaccard coefficient) and content-based features (e.g., content similarity between users' tweets).<br/>
**4.** **Model Training and Evaluation:** Splitting the dataset into training and validation sets, training a machine learning model using the extracted features, and evaluating the model's performance using metrics like precision, recall, and normalized discounted cumulative gain (nDCG) at different values of k, which represents the relevant elements to analyse.<br/>
**5.** **Recommendation Generation:** Using the trained model to predict links between users for a given set of user pairs, based on their network and content-based features.<br/>
**6.** **Results Visualization and Reporting:** Visualizing the results of the link prediction, including the predicted links and their associated probabilities, and reporting the performance of the model using appropriate evaluation metrics.

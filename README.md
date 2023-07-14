# Spotify App Store Review Sentiment Analysis 
![header](https://github.com/asoylatte03/spotify-app-reviews/blob/main/images/spotify-desktop-header.jpg)

#
**Author: Kevin Alexis Mendez*
## Prerequisites
This project was ran using a `WINx64` operating system. To replicate the environment used, download the `.txt` file located in the `requisites` folder in this repository. Running the following code will allow you to generate the same `conda env` used throughout this project.
```
conda env create -- file <file_name.txt>
```

## Business Understanding
Spotify is one of the leading providers for digital music streaming services. With podcasts, albums, songs, and even personalized playlists derived from user's listening history, Spotify has over 515 million active users worldwide as of 2023. Spotify provides users with both free and premium listening options with at least 317 million users on the free version of Spotify and 210 million premium subscribers globally. Spotify has one of the most diverse music libraries that provides users with the opportunity to listen to songs from diverse countries and cultures.

**Why Sentiment Analysis?**
Sentiment analysis is a technique used to derive sentiment from textual information. Use of sentiment analysis can provide companies and stakeholders with a more concrete understanding of their userbase. The conclusions derived from using sentiment analysis are broad but include:
1. **User experiences matter for product performance in post-production**
2. **Customer feedback can be used to provide better services and maintain a strong userbase**
3. **Sentiment analysis can provide an objective evaluation of how a project trends and generates media buzz and provide useful insights for brand advertising**

## Project Overview
This project seeks to build a binary classification model for predicting user sentiment from their reviews and provide insights into the Spotify user's experiences to establish key actions to consider when seeking to provide users with the best possible listening experience. 

## Data
Data was collected from [Kaggle](https://www.kaggle.com/datasets/mfaaris/spotify-app-reviews-2022) where reviews were scraped from the Google Play Store between January and July 2022. The original dataset contained features such as:
- User Reviews
- User Ratings (1-5)
- Total Thumbs Up
- Reply (Spotify's Customer Service Team response)

To extract the overall sentiment of a review, VADER was used to calculate the composite scores for each review. Using the composite scores, sentiment was classified as the following: 
- `comp_score` > 0 -> user review was positive 
- `comp_score` < 0 -> user review was negative
- `comp_score` == 0 -> user review was neutral 

## Method 
To accurately classify user sentiment based on their reviews, an iterative approach was used. First, `scikit-learn`'s `DummyClassifier` was used to create a baseline for evaluating model performance. Multiple classification algorithms were selected such as: 
- `Logistic Regression`
- `Multinomial Naive Bayes`
- `Complement Naive Bayes`
- `Bernoulli Naive Bayes`
- `XGBClassifier`

## Topic Modeling 
![topic_modeling](https://github.com/asoylatte03/spotify-app-reviews/blob/main/images/positive-reviews-topics.png)
To better understand the latent themes occurring in users with positive experiences, a topic model was performed. Four topics were found to capture the semantic information within positive reviews such as:
1. Topic 1: Spotify's Expansive Music Library
2. Topic 2: UI/UX Experiences
3. Topic 3: UX Evaluation of Spotify
4. Topic 4: Spotify's Algorithm
   
## Model Selection & Evaluation 
![log_reg](https://github.com/asoylatte03/spotify-app-reviews/blob/main/images/log_model_pr_auc.png)
For each classification algorithm used, a baseline model was constructed with default params and `TFIDFVectorizer` default params. Models were hyperparameter tuned and evaluated used the Precision-Recall AUC. The best model was a base `LogisticRegression` model with default params. 

## Key Actions
From model results, three key actions are proposed to improve user experiences with the Spotify app's functionality. 

### Added UX Functionality  
A recurrent theme from topic modeling positive user experiences was the customization inherent to the app. Users reported that having the ability to customize and add to personalized libraries and playlists to be a major plus when reviewing the app. Clearly, the addition of new features centered around UX/UI updates that provide more room for customization can provide a more positive experience for users.

### UX-Directed Algorithm Improvements
A point of praise and criticism were user's evaluation of Spotify's music library. Where the algorithm provided desired song reccommendations, users praised the algorithm for giving them a more enriching musical experience. However, where user's were left unsatisfied with the reccomendations provided, the algorithm become a point of contention. A UX-Derived approach to validating the different music reccomendations given to users would help alleviate the contentious attitudes towards the app and the algorithm as a whole.

### Bug Fixes
Where the model evaluated reviews to contain negative or positive sentiments, a recurrent theme were "bugs" and difficulties with the app's functionality. Having a more streamlined approach to addressing bugs as well as leveraging the responses by Spotify's Customer Service Team can aid in improving consumer relations and review sentiment.

## Acknowledgements & Credits 
Credit is given to `M Faarisul Ilmi` for scraping the data from the Google Play Store that this project uses. Check out his Kaggle profile [here](https://www.kaggle.com/mfaaris)
Statistics about Spotify were collected from `The Social Shepherd` and can be found [here](https://thesocialshepherd.com/blog/spotify-statistics)

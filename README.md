# Spotify App Store Review Sentiment Analysis 
![Gaming Setup](https://github.com/asoylatte03/osf_gaminganxiety/blob/main/images/blurrystock-HIbAmybJHVs-unsplash.jpg)

## Prerequisites
This project was ran using a `WINx64` operating system. To replicate the environment used, download the `.txt` file located in the `requisites` folder in this repository. Running the following code will allow you to generate the same `conda env` used throughout this project.
```
conda env create -- file <file_name.txt>
```

## Business Understanding
 

## Project Overview


## Data


## Method 


## Topic Modeling 
![topic_modeling](https://github.com/asoylatte03/spotify-app-reviews/blob/main/images/positive-reviews-topics.png)

1. Topic 1: Spotify's Expansive Music Library
2. Topic 2: UI/UX Experiences
3. Topic 3: UX Evaluation of Spotify
4. Topic 4: Spotify's Algorithm
   
## Model Selection & Evaluation 
![log_reg](https://github.com/asoylatte03/spotify-app-reviews/blob/main/images/log_model_pr_auc.png)


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

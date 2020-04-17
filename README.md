# Predicting YouTube Videos Views for Yoga Channels

## Problem statement

This project is aimed to explore the limits of what linear regression can do in terms of predictions of views per video. 

The dataset is scraped directly from YouTube using scripts located in the [scrape_scripts](https://github.com/elena-du/Metis-Project-2---Youtube-Predictions/tree/master/scrape_scripts) folder.

Final dataset is included as a binary file [here](https://github.com/elena-du/Metis-Project-2---Youtube-Predictions/blob/master/feature_engineering/video_channel_df_8162_fin.pkl). It contains 8162 observations and 25 features excluding actual number of video views and reference variables, such as channel name or URL.

## Results

Features with most predictive power are likes, dislikes and interactions of these variables, which is not surprising. It helps building pretty good inferencial linear regression model and studying linear relationships that comprise the recepie for views generation. Best model shows 0.99 R2 on Train and 0.77 R2 on Test sets.

The problem with this outcome is that you can infer, but cannot predict number of views for a new video as likes and dislikes are accumulated in parallel with views accumulation. I built a model that excluded likes and dislikes and got as high as 0.47 R2 with all features and interaction generated, regularization, and removing outliers. The latter was the most effective as classic assumptions of linear regression do not necesserily true for this set up.




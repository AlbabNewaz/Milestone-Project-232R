# Milestone-Project-232R
You can access to the ongoing notebook [here](https://colab.research.google.com/drive/1fRkPnDpM9iT9j1_r4wEPnfLOAMCwGa10?usp=sharing)

# Table Of Content:
[I. Introduction](https://github.com/AlbabNewaz/Milestone-Project-232R?tab=readme-ov-file#review-sentiment)

[II. Abstract](https://github.com/AlbabNewaz/Milestone-Project-232R?tab=readme-ov-file#abstract)

[III. Dataset](https://github.com/AlbabNewaz/Milestone-Project-232R?tab=readme-ov-file#dataset)

[IV. Processing Data](https://github.com/AlbabNewaz/Milestone-Project-232R?tab=readme-ov-file#processing-data)

[V. Data Exploration](https://github.com/AlbabNewaz/Milestone-Project-232R?tab=readme-ov-file#data-exploration)
- [Top Games](https://github.com/AlbabNewaz/Milestone-Project-232R?tab=readme-ov-file#top-games)
- [Scoring](https://github.com/AlbabNewaz/Milestone-Project-232R?tab=readme-ov-file#scoring)
- [Review Sentiment](https://github.com/AlbabNewaz/Milestone-Project-232R?tab=readme-ov-file#review-sentiment)

# Introduction

The following project takes data from Steam reviews and attempts to translate the data into digestible and understandable chunks for meaningful insights. 

# Abstract

This study analyzes a dataset of user reviews extracted from Steam to gain insights into player behavior and review patterns. The dataset includes comprehensive user review data, along with supporting metrics such as playtime, review timing, gameplay hours, and weighted user scores. By examining these key variables, this project seeks to uncover trends in how players engage with games, the relationship between play duration and review sentiment, and the potential impact of review timing on scoring behavior. The findings aim to contribute to a deeper understanding of user feedback dynamics in digital gaming platforms, offering valuable insights for both developers and researchers.

# Dataset

The database licensed by [MIT](https://www.mit.edu/~amini/LICENSE.md) and authored by [KieranPO'C](https://www.kaggle.com/kieranpoc) contains the following information:

- author
- steamid
- number of games owned
- number of reviews
- playtime all time
- playtime over the last 2 weeks
- playtime at the time of the review
- when they last played the game
- language
- time created
- time updated
- if the review was positive or negative
- number of people who voted the review up
- number of people who voted the review funny
- a helpfulness score (steam generated)
- number of comments
- if the user purchased the game on Steam
- if the user checked a box saying they got the app for free
- if the user posted this review while the game was in Early Access
- developer response (if any)

The dataset is roughly 40GB, expanding on 113,883,717 Steam reviews. 

# Processing Data

The following represents a general outline of cleaning and processing the dataset to be used for this report. 

1. Data Loading using Dusk due to the nature of the file size.
2. Initial Cleaning
   - Dropping rows with missing values
   - Dropping unwanted columns to increase performance.
   - Fixing data types
3. Filtering and sampling. Sampled only the top 20 for the initial data parsing to keep performance high and give an overall understanding of the data.
4. Grouping and aggregation to create visuals for us to interpret. 

# Data Exploration

### Top games
Diving into the data itself we can view some of the most reviewed games on Steam:
![image](https://github.com/user-attachments/assets/0334e365-7c05-470a-abce-3d73d547a8a7)
While not too insightful, it does prepare us for what games we would continue to see as we delve into the data.

### Scoring
Scoring behavior is also something to look into as some users tend to receive games for free while others pay for them. We can notice a postiive trend between recieving the game for free and reviewing the game more positively vs their paid counterparts other than a few exceptions.

![image](https://github.com/user-attachments/assets/6636fcdb-315b-425d-ad02-080a5f7c4b74)

### Review sentiment
The initial diagnosis of the diagram below shows that games tend to have a lower interquartile range for time played when there is a negative sentiment towards the game. This could be related to users quiting the game early after reviewing, while positive reviewers tend to continue playing for much longer. 
![image](https://github.com/user-attachments/assets/5d93ee69-21f0-488a-8b8d-46303fcae32e)
However, the data, at least for the top 20 games, does not show any strong trends to provide substantial evidence for any claims.


# Subreddit detection using NLP

## Overview
This project aims to detect the difference between two subreddits (in this case, the Chess subreddit and the chess subreddit) using Natural Languange Processing (NLP). The best performing machine learning models managed to identify the correct subreddit based of the title with a 69% accuracy, which is only slightly lower than the 72% achieved by when this was tried with human testing. 

---
### Data Collection

The Reddit API was used to scrape the title of 1000 subreddit posts dating from 2017 to 2021. 100 titles were scraped per subreddit, per year for these data ranges. (Reddit API: https://api.pushshift.io/reddit/search/submission)

--- 

### Data Analysis
#### Length of title 
The length of the title was analysed and used as a feature (Located: fetch_analysis.ipynb)

#### Polarity and Subjectivity
The polarity and subjectivity of the titles were measured using the TextBlob library. See the following for more info: https://textblob.readthedocs.io/en/dev/quickstart.html#sentiment-analysis

#### Part of Speech Tagging
Each title was split into individual words and then tagged based on its gramatical meaning. See the following for more info: https://www.nltk.org/book/ch05.html

#### Lemmazitation
The titles were also Lemmatized. See the following documentation for more info: https://www.nltk.org/_modules/nltk/stem/wordnet.html




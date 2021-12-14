<h1 style="text-align: center;"> ♟️ Subreddit detection using NLP ♟️ </h1>

## Overview
This project aims to detect the difference between two subreddits, in this case, the Chess subreddit and the AnarchyChess subreddit using Natural Languange Processing (NLP). The main difference between these subreddits is the Chess subreddit is more serious, with a significant amount of posts on learning chess and discussing chess seriously. In comparison, the AnarchyChess subreddit is not as serious with a lot of content containing humorous chess memes.

The model created could be used to allow reddit users to post in either the Chess or AnarchyChess subreddit and have them redirected to the appropriate subreddit based on the content of their post.

The best performing machine learning models managed to identify the correct subreddit based of the title with a 69% accuracy, which is only slightly lower than the 72% achieved by when this was tried with human testing. 

---
### Data Analysis
#### Popular words 
<img src="./graphs/word_art.png" alt="Drawing" style="width: 500px;"/>

#### Length of title 
The length of the title of each subreddit was compared and used as a feature. The chess subreddit titles are slighlty longer than AnarchyChess subreddit.

<img src="./graphs/reddit_title_length.png" alt="Drawing" style="width: 300px;"/>

#### Polarity and Subjectivity
The polarity and subjectivity of the titles were measured using the TextBlob library. Polarity measures sentiment between -1 and 1 (-1 being negative sentiment and 1 being positive sentiment). Subjectivity defines if a statement is more factual or opionated. The analysis showed that AnarchyChess users tended to use slightly more emotive languange compared to the Chess subreddit users.
<div align="center">
<img src="./graphs/reddit_subjectivity.png" alt="Drawing" style="width: 300px;"/>
<img src="./graphs/reddit_polarity.png" alt="Drawing" style="width: 300px;"/>
</div>

See the following for more info: [Textblob sentiment analysis documentation](https://textblob.readthedocs.io/en/dev/quickstart.html#sentiment-analysis)

#### Part of Speech Tagging
Each title was split into individual words and then tagged based on its gramatical meaning using the NLTK library. The Chess subreddit was found to be more gramatically correct.

See the following for more info: https://www.nltk.org/book/ch05.html

#### Stemming and Lemmatization
The titles were also stemmed and lemmatizated.

See the following documentation for more info: https://www.nltk.org/_modules/nltk/stem/wordnet.html

--- 
### Results 
Human identification of the subreddit showed the best results at 72% closely followed by Logistic Regression at 69%.
<div align="center">
<img src="./graphs/reddit_results.png" alt="Drawing" style="width: 300px;"/>
</div>

---
### Data Collection

The Reddit API was used to scrape the title of 1000 subreddit posts dating from 2017 to 2021. 100 titles were scraped per subreddit, per year for these data ranges. (Reddit API: https://api.pushshift.io/reddit/search/submission)


# Gesture Emoji Twitter Corpus

## Project Description

### 1. Collecting tweets

file 1: download_tweets.ipynb 

### 2. Data preprocessing

file 2: dataset_preprocessing.ipynb

### 3. Dataset: Engish

The dataset "Emoji Gestures in English Tweets: California" can be found here: https://zenodo.org/record/5802317#.YcTWIC-B1QJ

The dataset consists of 479 193 tweets. Each of them contains one of the 31 gesture emoji (different hand configurations) and its skin tone modifier options (e.g. 🙏🙏🏿🙏🏾🙏🏽🙏🏼🙏🏻). Tweets were posted within 250km from San Jose, CA and within 200km from Los Angeles, CA, in English, during May-August 2021. The dataset can be used to investigate the use of gesture emoji by English-speaking California Twitter users. Python libraries used for collecting tweets and preprocessing: tweepy, re, preprocessor, emoji, regex, string, nltk.

The dataset contains 12 columns:

-  *tweet_original* - original text of the tweet
-  *preprocessed* - preprocessed text of the tweet (4 initial steps)
-  *all_emoji* - lists all emoji in a given tweet
-  *hashtags* - lists all hashtags in a given tweet
-  *user_encoded* - encoded Twitter user name: the first 3 characters of the user name and the first 3 characters of the user's location
-  *location_encoded* - location of the user: "los_angeles", "san_diego", "san_jose", "san_francisco", "fresno", "long_beach", "sacramento", "oakland", "bakersfield", "anaheim", or "other"
-  *mention_present* - checks whether each tweet contains mentions
-  *url_present* - checks whether each tweet contains urls
-  *preprocess_tweet* - preprocessing step 1: tokenizing mentions, urls, and hashtags
-  *lowercase_tweet* - preprocessing step 2: lowercasing
-  *remove_punct_tweet* - preprocessing step 3: removing punctuation
-  *tokenize_tweet* - preprocessing step 4: tokenizing
    
### 4. Dataset: Russian

The dataset "Emoji Gestures in Russian Tweets: Moscow" can be found here: https://zenodo.org/record/5802328#.YcTWIS-B1QK

The dataset consists of 48 838 tweets. Each of them contains one of the 31 gesture emoji (different hand configurations) and its skin tone modifier options (e.g. 🙏🙏🏿🙏🏾🙏🏽🙏🏼🙏🏻). Tweets were posted within 50km from Moscow, Russia, in Russian, during May-August 2021. The dataset can be used to investigate the use of gesture emoji by Russian users of the Twitter platform. Python libraries used for collecting tweets and preprocessing: tweepy, re, preprocessor, emoji, regex, string, nltk. 

The dataset contains 12 columns:

-  *tweet_original* - original text of the tweet
-  *preprocessed* - preprocessed text of the tweet (4 initial steps)
-  *all_emoji* - lists all emoji in a given tweet
-  *hashtags* - lists all hashtags in a given tweet
-  *user_encoded* - encoded Twitter user name: the first 3 characters of the user name and the first 3 characters of the user's location
-  *location_encoded* - location of the user: "moscow", "moscow_region", or "other"
-  *mention_present* - checks whether each tweet contains mentions
-  *url_present* - checks whether each tweet contains urls
-  *preprocess_tweet* - preprocessing step 1: tokenizing mentions, urls, and hashtags
-  *lowercase_tweet* - preprocessing step 2: lowercasing
-  *remove_punct_tweet* - preprocessing step 3: removing punctuation
-  *tokenize_tweet* - preprocessing step 4: tokenizing
    
    

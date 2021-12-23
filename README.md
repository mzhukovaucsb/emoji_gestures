# Gesture Emoji Twitter Corpus

## Project Description

...

### 1. Data Collection (*download_tweets.ipynb*)

The first step in my project was to collect tweets using Python's *tweepy* library. The file *download_tweets.ipynb* contains a script to download tweets containing the character of interest (gesture emoji, in this case) given the chosen location and date, and returns text of the tweet, username, location, and date a tweet was written, saved into a .csv file. 

### 2. Data preprocessing (*dataset_preprocessing.ipynb*)

The second step in my project was to do text preprocessing using Python libraries *re, preprocessor, emoji, regex, string, nltk*. The file *dataset_preprocessing.ipynb* contains several functions: 

-  *hashtags* - returns a list of hashtags for each tweet thath contains hashtags
-  *encoding_username* - encodes user names combining the first 3 characters of the user name and the first 3 characters of the user's location
-  *all_emoji_tweet* - returns a list of all emoji that each tweet contains
-  *preprocess_tweet* - for each tweet, tokenizes hashtags, urls, and mentions
-  *lowecase_tweet* - lowercasing for each tweet
-  *remove_punct_tweet* - removes punctuation marks for each tweet
-  *tokenize_tweet* - tokenizes each tweet
-  *preprocessed* - puts all the stage of preprocessing together
-  *url* - for each tweet, checks in the tweet contains urls
-  *mention* -  for each tweet, checks in the tweet contains mentions
-  *hashtag* - for each tweet, checks in the tweet contains hashtags


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
    
    

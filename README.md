# Gesture Emoji Twitter Corpus

## Project Description

Emoji started to be used by Internet users only 20 years ago, and since that time the multidisciplinary field of emoji studies has also begun to actively develop (Tang and Hew 2019). Emoji can be conceptualized as a non-verbal cue in computer-mediated communication, used to enhance or replace text with certain emotions or conceptualizations. There is great potential for insight from research that considers questions of what functions emoji gestures represent in computer-mediated communication, how the self-representation of social media users is constructed through the use of gesture emoji that represent body parts, and whether there is a relationship between the use of emoji gestures in computer-mediated communication and the use of co-speech gestures in conversation. Such studies require an annotated dataset containing a sufficient number of examples for each emoji to give researchers the opportunity to examine different examples of emoji use and to perform computer-mediated discourse analysis. 

Over Summer 2021, I collected over 500,000 tweets that contain one of the 31 gesture emoji (different hand configurations) and its skin tone modifier options (e.g. 🙏🙏🏿🙏🏾🙏🏽🙏🏼🙏🏻) in English and Russian and compiled the data into 2 datasets, having performed text processing as well. The results of the project are as follows: the code for the tweet collection, and the code for tweet preprocessing, and 2 datasets with documentation. 

This repository presents the code for tweet collection and tweet preprocessing and provides the links to two two datasets containing tweets with gesture emoji posted by Twitter users over the summer of 2021 in Russian and English. The datasets are published on Zenodo for public use by scholars in the field of emoji and gesture studies. 

The list of emoji (hand gestures and their skin tone modifier options)

|  # | Emoji | Description (Emojipedia 2021)  |
| ------------- | ------------- | ------------- |
| 1  | 👋👋🏿👋🏾👋🏽👋🏼👋🏻  | Waving Hand |
| 2  | 🤚🤚🏿🤚🏾🤚🏽🤚🏼🤚🏻  | Raised Back of Hand  |
| 3  | 🖐️🖐🏿🖐🏾🖐🏽🖐🏼🖐🏻  | Hand with Fingers Splayed  |
| 4 | ✋✋🏿✋🏾✋🏽✋🏼✋🏻  | Raised Hand  |
| 5  | 🖖🖖🏿🖖🏾🖖🏽🖖🏼🖖🏻  | Vulcan Salute |
| 6  | 👌👌🏿👌🏾👌🏽👌🏼👌🏻  | OK Hand  |
| 7  | 🤌🤌🏿🤌🏾🤌🏽🤌🏼🤌🏻 | Pinched Fingers|
| 8  | 🤏🤏🏿🤏🏾🤏🏽🤏🏼🤏🏻  | Pinching Hand |
| 9  | ✌️✌🏿✌🏾✌🏽✌🏼✌🏻  | Victory Hand  |
| 10  | 🤞🤞🏿🤞🏾🤞🏽🤞🏼🤞🏻  | Crossed Fingers  |
| 11  |  🤟🤟🏿🤟🏾🤟🏽🤟🏼🤟🏻  |  Love-You Gesture  |
| 12  | 🤘🤘🏿🤘🏾🤘🏽🤘🏼🤘🏻  | Sign of the Horns  |
| 13  | 🤙🤙🏿🤙🏾🤙🏽🤙🏼🤙🏻  | Call Me Hand |
| 14  | 👈👈🏿👈🏾👈🏽👈🏼👈🏻  | Backhand Index Pointing Left  |
| 15  | 👉👉🏿👉🏾👉🏽👉🏼👉🏻  | Backhand Index Pointing Right   |
| 16  | ☝️☝🏿☝🏾☝🏽☝🏼☝🏻  | Backhand Index Pointing Up |
| 17  | 🖕🖕🏿🖕🏾🖕🏽🖕🏼🖕🏻  | Middle Finger |
| 18  | 👇👇🏿👇🏾👇🏽👇🏼👇🏻 | Backhand Index Pointing Down |
| 19  | ☝️☝🏿☝🏾☝🏽☝🏼☝🏻 | Index Pointing Up |
| 20  | 👍👍🏿👍🏾👍🏽👍🏼👍🏻 | Thumbs Up |
| 21  | 👎👎🏿👎🏾👎🏽👎🏼👎🏻 | Thumbs Down |
| 22  | ✊ ✊🏿✊🏾✊🏽✊🏼✊🏻 | Raised Fist|
| 23  | 👊👊🏿👊🏾👊🏽👊🏼👊🏻 | Oncoming Fist  |
| 24  | 🤛🤛🏿🤛🏾🤛🏽🤛🏼🤛🏻  | Left-Facing Fist  |
| 25  | 🤜🤜🏿🤜🏾🤜🏽🤜🏼🤜🏻  | Right-Facing Fist   |
| 26  | 👏👏🏿👏🏾👏🏽👏🏼👏🏻    |Clapping Hands |
| 27  | 🙌 🙌🏿 🙌🏾 🙌🏽 🙌🏼 🙌🏻   |  Raising Hands |
| 28  | 👐👐🏿👐🏾👐🏽👐🏼👐🏻  |  Open Hands |
| 29  | 🤲🤲🏿🤲🏾🤲🏽🤲🏼🤲🏻 | Palms Up Together  |
| 30  | 🙏🙏🏿🙏🏾🙏🏽🙏🏼🙏🏻  | Folded Hands  |
| 31  | 🤝  | Handshake  |

### 1. Data Collection (*download_tweets.ipynb*)

The first step in my project was to collect tweets using Python's *tweepy* library. The file *download_tweets.ipynb* contains a script to download tweets containing the character of interest (gesture emoji, in this case) given the chosen location and date, and returns the text of the tweet, username, location, and date a tweet was written, saved into a .csv file. 

### 2. Data preprocessing (*dataset_preprocessing.ipynb*)

The second step in my project was to do text preprocessing using Python libraries *re, preprocessor, emoji, regex, string, nltk*. The file *dataset_preprocessing.ipynb* contains several functions: 

-  *hashtags* - returns a list of hashtags for each tweet that contains hashtags
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

The dataset contains 11 columns:

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

The dataset contains 11 columns:

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
    
    

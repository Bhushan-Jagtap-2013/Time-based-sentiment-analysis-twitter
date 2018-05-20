# Time Based Sentiment Analysis Twitter
Allows the user to analyze Twitter sentiment based on selected time event  and visualizes  the results


## Group Members :

* Vishal Kudale
* Kartik Joshi
* Bhushan Jagtap

## 1. Introduction:

Allow user to provide a hashtag as input and gather all the data related to given hashtag (E.g. #GunReform). Perform sentiment analysis on extracted tweets and plot that on time series format.  Along with Time series data plotting, plot Geolocation data, Devices used for tweeting, and information like count of unique users, tweet’s likes, re-tweets etc.

As part of dynamic implementation user can select a date. According to date selected by user ‘before-and-after sentiment analysis graph’ will be updated. The main purpose of this implementation is to determine how people have reacted to specific event (such as parkland mass shooting), at what extent they used twitter to express their thoughts and how the response has been formed over the time. Also, information like number of tweets, likes, unique tweets etc. can help us to have a good visualization on many technical aspects.


## 2. How to run:

Step 1: Specify user authentication data in auth_dict file.
Step 2: Install dependencies if required.
Step 3: You can run entire project as we have provided pre-trained classifier as well as sample database for ‘gunreform’ hashtag.
Step 4: select date against which you would like to analyze tweets and accordingly graph will be updated.
Step 5: At end of Jupiter notebook we have given code to gather data for new hashtags and a way to download sample_tweets data set to retrain classifier. 

## 3. Dependencies:

[Note: We are using bokeh version 0.12.7 on our system for development]

Installing dependencies using conda (install conda if required):

``` bash
python -m bokeh info
conda uninstall bokeh
conda install bokeh=0.12.7
conda install NumPy
conda install blaze
conda install dask
conda install pandas
```

Installing dependencies using pip:


```  bash 
pip install jsonpickle
pip install tweepy
pip install -U nltk
```

## 4. How project works:

#### 1.User Enters Hashtag
We have provided a text box where user can input all the hashtags on which he wants to perform time-based analysis.

#### 2. Gathering information from twitter and perform sentiment analysis 
Once we have all the hashtags user want to search, we will query to twitter using tweepy API to get all tweets related to hashtags.

#### 3. Preprocess data and sentiment analysis
Once we have all the information related to hash tags we will extract following fields from it:

----
Tweet_Ids, User_Ids, Date, ReTweet_Count, Location, Likes, TweetSource, Actual tweets
----


Then we will perform sentiment analysis on tweets and we will store all information along with tweet sentiment in database for further analysis and visualization.

#### 4. Acceptance of analysis date from user
We have provided a drop-down list for user from which user can select a date on which user want to divide tweets. This division of tweets will be used to analyze the effect of selected date on tweets and user sentiment.

#### 5. Visualize results
Once we have all the processed information we can visualize the results based on date entered by user using graphs such as time series, geo-plot, sentiment analysis bar graph etc.


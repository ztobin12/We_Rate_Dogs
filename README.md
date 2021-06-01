# We_Rate_Dogs Wrangling Project

## Introduction
Data Wrangling is an important and necessary step to data analysis. For data wrangling there are three parts: gathering, assessing, and cleaning. Gathering consists of finding the right datasets. Assessing consists at looking at the dataset and finding both quality and tidiness issues. Cleaning consists of using code to fix the issues you found when assesing. The dataset that we will be wrangling (and analyzing and visualizing) is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs.


## Step 1: Gather Data
The Data is gathered from 3 resources:

The We Rate Dogs Twitter archive. This was downloaded manually using Udacity servers. This data was put into a data set called twitter_archive.
The image predictions file. This was downloaded programatically via Udacity servers. This data was put into a data set called image_predictions.
Each tweets retweet count and favorite count, by using the tweet IDs, which gave me the chance to query Twitter API, for each tweet's JSON data, in a file called tweet_json.txt file, using Python's tweepy library. This data was put into a dataframe called tweet_df.
Once when all the data was gathered it as imported into a Jupyter Notebook.

## Step 2: Assess The Data
The objective was to find eight quality issues, and two tidiness issues. In order to do this, all three data sets needed to be visually assessed an reviewed.

### Step 2A: Find Quality Issues
Quality issues include completeness, validity, accuracy, and consistentcy. Some of the quality issues found here are:

The first issue that needed to be fixed is that retweets need to be dropped from the data set.
In_reply_status_id, in_reply_to_user_id, retweeted_status_id, and retweeted_status_user_id are incomplete.
Favorite_count, timestamp, and retweet_count are all incorrect datatypes.
Sources column can be removed
Some of the names feature 'a', 'an' and 'the'
Some of the names aren't capitalized.
The rating_denominator has values other 10
The rating_numerator has some outliers that should be dropped.
### Step 2B: Find Tidiness Issues
Tidiness issues are ways to make the data set more compact and easier to interpet. This includes:

Merging the datasets into one Dataframe.
Combining the doggo, floofer, pupper, and puppo into one column
Combining the rating_numerator and rating_denominator into one column
## Step 3: Clean the Data
The first The first step of cleaning was to merge all three data sets into one frame, as this made it much easier to clean and analyze the data. It is called DF_Master. From this point we can go through each issue, and make sure to define the problem, fix it with coding, and then lastly test it to make sure it ran smoothly.


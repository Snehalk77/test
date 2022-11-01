## Project Abstract
A person's inner athlete often emerges when discussing sports. Everyone develops a niche or a preference for certain sports-related subjects or athletes. The key idea here is that each person makes an effort to become an authority in the sport about which they have an opinion or even just express a general interest in the current sporting event. We want to show the trends in sports over a period of time.

## Team - SocialGeeks

* Sameer Chaudhari, schaud24@binghamton.edu
* Snehal Karwa, skarwa1@binghamton.edu
* Pratik Upadhyay, pupadhy3@binghamton.edu

## Tech-stack
* 'python' - The project is developed and tested using python v3.9. [Python Website](https://www.python.org/)
* 'request' - Requests is a python library which allows you to send HTTP/1.1 requests extremely easily. [Request Website](https://pypi.org/project/requests/)
* 'pymongo'- This project uses NoSQL database MongoDB to store the collected data
    * [MongoDB Website](https://www.mongodb.com/)
    * [Python MongoDB Adapter - pymongo](https://pymongo.readthedocs.io/en/stable/)
* 'schedule' - Schedule is a python library which run python functions periodically using a friendly syntax. [Schedule Website](https://pypi.org/project/ schedule/)

* 'datetime'  - datetime is a python library which can be used for manipulating dates and times. [datetime Website](https://pypi.org/project/DateTime/)
* 'sys'  - Sys module provides access to some variables used or maintained by the interpreter and to functions that interact strongly with the interpreter 
	   [Sys Website](https://docs.python.org/3/library/sys.html)
* 'json'  - JSON is a syntax for storing and exchanging data. [json Website](https://docs.python.org/3/library/json.html)


## Data Source

This section must include two things for each source: (1) A specific end-point URL(aka API) or Website link if you are crawling web-pages (2) Documentation of the API

* `Twitter`
  * [Volume Stream API](https://developer.twitter.com/en/docs/twitter-api/tweets/volume-streams) - API provided by Twitter Inc. to fetch 1% of all tweets that are tweeted in real time

* `Reddit` - We are using 'r/sports', 'r/cricket', etc.
  * [API](https://www.reddit.com/dev/api#GET_comments_{article}) - api for collecting comments from particular subreddit

  * [r/sports](https://reddit.com/r/sports) - sports subreddit will collect information about all sports
  * [API-1](https://reddit.com/r/sports/comments) - collecting comments from subreddit sports

  * [r/cricket](https://reddit.com/r/cricket) - sports subreddit will collect information about cricket
  * [API-1](https://reddit.com/r/cricket/comments) - collecting comments from subreddit cricket

  * [r/football](https://reddit.com/r/football) - sports subreddit will collect information about football
  * [API-1](https://reddit.com/r/football/comments) - collecting comments from subreddit football

  * [r/mlb](https://reddit.com/r/mlb) - sports subreddit will collect information about all mlb
  * [API-1](https://reddit.com/r/mlb/comments) - collecting comments from subreddit mlb

  * [r/nfl](https://reddit.com/r/nfl) - sports subreddit will collect information about all nfl
  * [API-1](https://reddit.com/r/nfl/comments) - collecting comments from subreddit nfl

  * [r/nba](https://reddit.com/r/nba) - sports subreddit will collect information about all nba
  * [API-1](https://reddit.com/r/nba/comments) - collecting comments from subreddit nba

  * [r/tennis](https://reddit.com/r/tennis) - sports subreddit will collect information about all tennis
  * [API-1](https://reddit.com/r/tennis/comments) - collecting comments from subreddit tennis

* `4chan`
  * [API-Endpoint](https://a.4cdn.org/sp/catalog.json) - Publically available API endpoint to retrieve comments from '/sp/' (Sports) Board
  * [Website-link](https://github.com/4chan/4chan-API) - Data from the 4chan API is exclusively accessible from a.4cdn.org, via either http:// or https:// protocols


## How to run the project?

Install `Python` and `MongoDB`

```bash
pip install requests,schedule,pymongo

#run twitter script
python twitterAPI.py <context>

#run reddit script
python redditAPI.py subreddit_name.text

#run 4chan script
python chanAPI.py

```

## Database schema - NoSQL MongoDB

```bash

collection_1: twitter_volume
{
  "id": ...,
  "Tweet": ...,
  "Author_ID": ...,
  "Tweet_Time": ...,
  "Sports_Tweet": ...
}

collection_1: twitter_count
{
  "id": ...,
  "Tweet_Count": ...,
  "Sport_Count": ...
}

collection_2: reddit_comments
{
  "id": ...,
  "Subreddit": ...,
  "Title": ...,
  "Comment": ...,
  "Comment_Time": ...
}

collection_3: 4chan_posts
{
  "id": ...,
  "text": ...,
  "timestamp": ...
}
```


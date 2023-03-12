# Data Set Creation

## 1) Sources of the Data

### 1a) Where did you get the data?

This data set comes from the r/nba subreddit on Reddit. This is a community for discussion about all topics around the NBA including news, game threads, and general viewpoints. The data includes the top 1000 threads from this subreddit in the past year to date (03/11/2023). They are rated based on the number of upvotes each thread has received. 

### 1b) How did you get the data?

I gathered the data from the r/nba subreddit using the Python Reddit API Wrapper (PRAW) library. This API allowed me to systematically collect discussion threads and their data including their id, title, text, and comments. The documentation for the API can be found [here](https://praw.readthedocs.io/en/stable/getting_started/quick_start.html)

### 1c) What is the license of the data if any?

I did not find any restrictive license on the use of the data. All I found were rules about using the API outlined [here](https://github.com/reddit-archive/reddit/wiki/API).

### 1d) Link to the get the data:

The code to get the data can be found [here](project_notebooks/data_set_creation.ipynb). 

The actual dataset can be found [here](nba_reddit_threads_data.csv).

## 2) Description of the Data

### 2a) What is the size of the dataset?

The dataset consists of 1000 rows. The file size is 1,634 kb.

### 2b) What is the format of the dataset?

The dataset is a CSV file with 4 columns and 1000 rows.

### 2c) What is the structure of the dataset?

The CSV file has 4 columns. The first column is a string representing the "thread_id". This is a unique id given to the discussion thread and retrieved using the API. It can be used as a unique identifier. 

The second column is titled "thread_title." This is a string representation of the title given to the thread by the original author. This title can give some insight into the contents or topic of the thread.

The third column is titled "thread_comments." This column consists of lists that have 10 strings each. Each of those strings is a comment from the thread. The included strings in the list are the top 10 upvoted comments from that thread. This indicates the most engaged with comments and provides a baseline for what opinions were popular in that thread. Since there are a total of 1,000 threads and 10 comments per thread, there are a total of 10,000 comments in the data set. 

The final column is "thread_text." This is a string that, if available, is the text written by the original author of the thread. If the thread was a link to a video, tweet, or other external source with no text, the entry is a "None" type object. 

To make the dataset have each row represent comments instead of threads, the CSV can be exploded on the "thread_comments" column which results in 10,000 rows. The current dataset does not have that configuration, though.

## 3) Data Models and Data Structures

### 3a) What are the data models used in the dataset? 

The data model is a relational model because it is a table/CSV. It could be loaded into a SQL database if desired. 

### 3b) What are the data structures used in the dataset?

The data structure is a set of arrays that makes up each column of the CSV. These arrays contain either strings or lists of strings. The table below outlines the data type for each column of the data set. 

| Column Title | Data Type |
| ------- | -------- |
| "thread_id"  | string |
| "thread_title" | string |
| "thread_comments" | list |
| "thread_text" | string |
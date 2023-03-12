## DATA 340: NLP Course Project
### Project Question and Goals

In this project, I hope to better understand how fans talk about the NBA and its players. The place I plan on gathering this data is from the subreddit [r/NBA](https://www.reddit.com/r/nba/). In this subreddit, there is common discourse about games and players. I have a long list of questions to better understand the discourse around the teams and players. What players are talked about the most? Are the players who are mentioned the most talked about favorably or unfavorably? Are there players who are talked about disproportionally to their impact on the court? What team gets the most coverage? Conversely, which teams are talked about the least frequently? This list of questions is long sprawling and likely to expand throughout the project. My desire to answer these questions stems from my love of the NBA as well as the conversations and discourse around it. I know that I have certain perspectives on how that discourse is shaped, but I am curious if my assumptions match up with the truth. Maybe I only see a fraction of the opinions fans share and there is a whole group that has different views than I do. I want to uncover these facts and have a better understanding of the NBA community as a whole. Answering these questions will give a better understanding of how the NBA community on Reddit feels and acts.

### Project Timeline

- Gather the data from the subreddit using a reddit API. The API I will use is the Python Reddit API Wrapper (PRAW)
- Once I have the data, I will need to do preprocessing and exploratory analysis. This includes tokenization using the NLTK library to distill words to their root. 
- One complication with the preprocessing could be dealing with short-hand, misspelled, or slang words that could be in the text due to it being an online format. I will need to find a way to deal with these. 
- Isolate text based on teams or players mentioned in the text. Calculate word frequency counts for teams and players. With this, decide which players are talked about the most or least. Potentially graph these findings.
- Isolate adjectives used to describe these teams and players in bigrams or trigrams. 
- Calculate the frequency of adjectives and compare for players and teams.
- Perform a sentiment analysis of the adjectives used for players and teams to understand how they are talked about.

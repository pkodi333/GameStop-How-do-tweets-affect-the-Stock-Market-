# GameStop-How-do-tweets-affect-the-Stock-Market-

GameStop became a poster child for meme stock Trade as there was a 1600% rally in stock price. Thus, it became influential for the common man to invest in it.
 
In this project, I did the following:
Analyzed how twitter reacted to the frenzy and got insights on the shift in sentiment 
Analyzed if the shift in sentiment is impacts stock price movement or not for the next day

LDA was used for topic modeling and VADER for the sentiment analysis.

I extracted the tweets with hashtags GME and GameStop time periods i.e., Oct'20-Dec'20 (Pre), Jan'21-Mar'21 (frenzy period) and Apr'21-Sep'21 (Post) using snscraper.

I cleaned the data by removing punctuations, URLs, hyperlinks, emojis, stopwords and frequently appearing collection of words (ex: gamestop, gme, game,  ps5, xbox etc.) I obtained the individual words from the sentences with lemmatization.

According to our topic modeling for the Post period, it is observed that the frenzy related to the GameStop as a memestock slowly started dying down and the stock price may start stabilizing.

Using the SentimentIntensityAnalyzer from VADER, we can check whether the tweet has a positive, negative, or neutral sentiment and the score tells us the intensity. 

a. If the compound score >= 0.05, then the sentiment is positive
b. If the compound score <= -0.05, then the sentiment is negative
c. If the compound score < 0.05 and > -0.05, then the sentiment is neutral

Then I compared each day's opening price with the number of positive tweets to see if the number of positive tweets increased with respect to previous day and there was an increase in opening price with respect to previous day. Result: In less than half of the occasions, the tweet sentiment reflected the next day's stock movement.

We cannot conclusively state that the positive sentiment in twitter led to increase in stock prices because there are many other external factors involved which drive the stock price movement, but we can use this analysis in a more directional and indicative manner. This cannot be used as a tool for long term investments.

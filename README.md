# GameStop-How-do-tweets-affect-the-Stock-Market-

GameStop became the poster child of the meme stock movement in early 2021, with a 1600% rally that caught Wall Street by surprise. This project investigates whether Twitter sentiment had any measurable influence on GameStop’s stock price and if social media hype could be used as an early signal for price movement.

We use **VADER** for sentiment analysis and **LDA** for topic modeling on tweets that mention `#GME` or `#GameStop` from different time periods (Pre-hype, Hype, and Post-hype) to explore changes in public sentiment and their potential correlation with daily stock price movements.

---

## 🧪 Objective

- Analyze how Twitter sentiment shifted before, during, and after the GameStop frenzy
- Evaluate if sentiment on Twitter can help predict next-day stock price movement

---

## 📊 Data Collection

- Tweets were extracted using `snscrape` with hashtags `#GME` and `#GameStop`
- Time periods analyzed:
  - **Pre-Hype**: Oct 2020 – Dec 2020
  - **Hype Period**: Jan 2021 – Mar 2021
  - **Post-Hype**: Apr 2021 – Sep 2021

---

## 🔧 Tools & Libraries

- Python (Pandas, NumPy, Matplotlib, Seaborn, NLTK, Gensim)
- VADER (Sentiment Analysis)
- LDA (Topic Modeling)
- snscrape (Twitter scraping)

---

## 🧹 Data Cleaning

- Removed:
  - Punctuation
  - URLs and hyperlinks
  - Emojis and HTML tags
  - Stopwords and high-frequency terms (e.g., "gamestop", "game", "ps5", "xbox")
- Applied lemmatization to normalize text

---

## 🗣️ Sentiment Analysis

Used VADER's `SentimentIntensityAnalyzer` to classify sentiment:

- **Positive**: Compound score ≥ 0.05  
- **Negative**: Compound score ≤ -0.05  
- **Neutral**: -0.05 < Compound score < 0.05  

Daily average sentiment was compared to next-day stock price movement to assess correlation.

---

## 🧵 Topic Modeling

Used **Latent Dirichlet Allocation (LDA)** to identify tweet topics:

- During the **Post-Hype** period, results showed a clear drop-off in meme-related or hype-driven language.
- Indicates waning public attention and normalization of GameStop stock discussions.

---

## 📈 Results & Observations

- In **less than half** of the cases, Twitter sentiment aligned with next-day stock price movement.
- Sentiment shifted significantly during the Hype phase, driven by FOMO, short squeeze narratives, and retail investor solidarity.
- Post-Hype tweets became more rational and less speculative.

---

## 🤔 Conclusion

While Twitter sentiment showed **some directional clues**, it did **not reliably predict next-day price movement**. Market behavior is influenced by numerous external variables—this analysis serves more as a **social signal tracker** than a forecasting tool.

> 📝 **Takeaway**: Use sentiment as a supporting indicator, not a standalone investment strategy.

---

## 📎 Future Improvements

- Incorporate Reddit sentiment (e.g., r/WallStreetBets)
- Explore lagged sentiment effects over 3–5 days
- Integrate volume and volatility indicators for stronger modeling

---

## 📁 Repository Structure


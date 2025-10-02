# Trading Behavior vs. Market Sentiment Analysis

## 📖 Project Objective

This project performs an in-depth analysis of the relationship between trader behavior and overall market sentiment. By leveraging historical trading data and the daily Fear & Greed Index, the analysis aims to identify hidden trends and actionable signals that can inform smarter, data-driven trading strategies.

The primary goal is to answer the question: **How do trading profitability, risk, and volume align or diverge from the prevailing emotions of fear and greed in the market?**

-----

## 📊 Data Sources

This analysis utilizes two key datasets:

  * **`historical_data.csv`**: Contains anonymized, transactional-level trading data, including trade size, direction (buy/sell), and realized profit and loss (PnL).
  * **`fear_greed_index.csv`**: Contains the daily historical values of the crypto Fear & Greed Index, which quantifies market sentiment.

-----

## ⚙️ Analytical Approach

1.  **Data Preprocessing**: Cleaned and formatted both datasets. Timestamps were converted to a consistent `datetime` format.
2.  **Data Merging**: The trading data was merged with the sentiment data on a daily basis to link each trade to the prevailing market sentiment.
3.  **Exploratory Data Analysis (EDA)**: A comprehensive EDA was conducted to analyze:
      * The distribution and cyclical nature of market sentiment.
      * The characteristics of trader behavior (PnL, volume).
      * The correlation between trading metrics and sentiment scores.
4.  **Visualization**: Key relationships were visualized using Matplotlib and Seaborn to make the findings clear and interpretable.

-----

## 💡 Key Findings & Insights

The analysis revealed a strong contrarian relationship between trader behavior and market sentiment.

1.  **Fear is a Buying Opportunity**: Periods of 'Extreme Fear' are correlated with a significant increase in **BUY** orders, suggesting traders are "buying the dip."
2.  **Greed is a Selling Signal**: Periods of 'Extreme Greed' are correlated with an increase in **SELL** orders, indicating that traders are taking profits when the market is euphoric.
3.  **Emotional Extremes Drive Volume**: Trading volume is highest during periods of both 'Extreme Fear' and 'Extreme Greed', highlighting that emotional markets are the most active and volatile.

> **Conclusion**: The data suggests that a profitable strategy involves acting contrary to the crowd—buying when others are fearful and selling when they are greedy.

-----

## 📈 Visualizations

The following visualizations were generated to support the analysis:

  * **Fear & Greed Index Over Time**: A line chart showing the cyclical nature of market sentiment.
  * **Distribution of Market Sentiment**: A bar chart illustrating the frequency of each sentiment category.
  * **Profit and Loss vs. Market Sentiment**: A boxplot revealing higher PnL volatility during periods of 'Extreme Fear'.
  * **Total Trading Volume vs. Market Sentiment**: A bar chart showing that volume peaks at sentiment extremes.
  * **Trading Side (Buy/Sell) vs. Market Sentiment**: A count plot that clearly illustrates the contrarian buying and selling patterns.

*(In a real README, you would embed the image files here, e.g., `![PnL vs. Sentiment](images/pnl_vs_sentiment.png)`)*

-----

## 🚀 Setup & Usage

To replicate this analysis, follow these steps:

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/your_username/trading-sentiment-analysis.git
    cd trading-sentiment-analysis
    ```

2.  **Install dependencies:**
    Make sure you have Python 3 installed. Then, install the required libraries.

    ```bash
    pip install pandas numpy matplotlib seaborn
    ```

3.  **Place the data:**
    Ensure `historical_data.csv` and `fear_greed_index.csv` are in the root directory of the project.

4.  **Run the analysis script:**

    ```bash
    python analysis.py
    ```

    The script will process the data and display the visualizations on your screen.

-----

## ⚠️ Limitations

  * The analysis of **leverage** was not possible as this data was not present in the provided dataset.
  * The analysis is based on historical data and does not guarantee future performance.
  * The trading data is anonymized, so no conclusions can be drawn about specific trader demographics or strategies.

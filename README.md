# analysis.ipynb

Objective

The goal of this project is to analyze how Bitcoin market sentiment (Fear vs Greed) relates to trader behavior and performance on the Hyperliquid platform. The analysis aims to uncover actionable patterns that can inform smarter trading strategies and risk management rules.

Datasets

Bitcoin Market Sentiment (Fear/Greed Index)

Columns: timestamp, value, classification, date

Represents daily market sentiment as Fear or Greed.

Historical Trader Data (Hyperliquid)

Columns include:
Account, Coin, Execution Price, Size Tokens, Size USD, Side,
Timestamp IST, Closed PnL, Direction, etc.

Contains trade-level data for multiple traders.

Tech Stack

Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn (for bonus modeling & clustering)

Jupyter Notebook


⚙️Setup & How to Run

Clone the repository:

git clone <your-repo-url>
cd trader-sentiment-analysis


Create and activate a virtual environment (optional but recommended):

python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate

Install dependencies:

pip install -r requirements.txt


(If you don’t have a requirements.txt yet, install manually:)

pip install pandas numpy matplotlib seaborn scikit-learn jupyter


Run the notebook:

jupyter notebook


Open analysis.ipynb and run cells top-to-bottom.


 🧹 Data Preparation

Parsed timestamps from both datasets and aligned them at daily granularity.

Cleaned and standardized column names for consistency.

Created derived metrics such as:

Daily PnL per trader

Win rate

Number of trades per day

Average trade size

Long/Short ratio

Merged trader activity with daily Fear/Greed sentiment.



📊 Key Analysis

The following questions were explored:

Does trader performance (PnL, win rate) differ between Fear and Greed days?

Do traders change their behavior (trade frequency, size, leverage) based on sentiment?

How do different trader segments behave under different sentiment regimes?

🔍 Key Insights

Traders generally achieve higher average PnL and win rates during Greed days compared to Fear days.

Trade frequency and trade sizes tend to increase during Greed periods, indicating higher risk appetite.

Frequent and consistent traders benefit more from Greed phases, while inconsistent traders experience larger drawdowns during Fear phases.

(Refer to charts in the notebook for supporting evidence.)


🧠 Actionable Strategy Recommendations

Risk Control During Fear:
During Fear days, reduce position sizes and leverage for high-frequency or inconsistent traders to limit drawdowns.

Selective Aggression During Greed:
During Greed days, allow increased trading activity only for historically consistent or profitable traders to maximize upside while controlling risk.


⭐ Bonus Work
🔮 Predictive Modeling

A simple Random Forest classifier was trained to predict whether a trader would be profitable on a given day using sentiment and behavioral features (trade frequency, win rate, trade size). Feature importance analysis highlights win rate and activity level as key drivers of profitability.

👥 Trader Clustering

Traders were clustered into behavioral archetypes using KMeans based on PnL, volatility, trade frequency, and directional bias. The resulting clusters reveal distinct trading styles that can be targeted with different strategy rules.


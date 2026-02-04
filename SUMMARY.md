Methodology

I analyzed two datasets: the Bitcoin Fear & Greed Index (daily sentiment labels) and Hyperliquid trader-level historical data. Trade timestamps were parsed and aligned to daily granularity, then merged with daily market sentiment. I standardized column names and engineered key behavioral and performance metrics including daily PnL per trader, win rate, number of trades per day, average trade size, and long/short bias.

For analysis, I compared trader performance and behavior across Fear vs Greed days using aggregated statistics and visualizations (bar charts and boxplots). I also segmented traders based on trading frequency and PnL stability to examine heterogeneous responses to market sentiment. As a bonus, I built a simple predictive model to estimate daily profitability using sentiment and behavioral features, and clustered traders into behavioral archetypes.

Key Insights

Performance differs by sentiment regime: Average daily PnL and win rates are higher during Greed days compared to Fear days, indicating more favorable trading outcomes when market sentiment is positive.

Behavior changes with sentiment: Traders increase activity and trade size during Greed periods, reflecting higher risk appetite, while Fear days show reduced participation and more conservative positioning.

Segments respond differently: Frequent and consistent traders benefit more from Greed phases, whereas inconsistent traders experience larger drawdowns during Fear days. This suggests sentiment amplifies existing strengths and weaknesses across trader types.

Strategy Recommendations

Risk control during Fear days: Cap leverage and reduce position sizes for high-frequency or inconsistent traders during Fear periods to limit drawdowns and protect capital.

Selective aggression during Greed days: Allow increased trade frequency or position sizing during Greed periods only for historically consistent or profitable traders to capture upside while managing downside risk.

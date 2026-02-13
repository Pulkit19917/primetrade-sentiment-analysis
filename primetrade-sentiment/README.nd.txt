📊 PrimeTrade Sentiment Analysis

Behavioral & Performance Analysis of Traders Across Market Sentiment Regimes

📌 Project Overview

This project analyzes how trader behavior and performance vary across different market sentiment regimes (Extreme Fear → Extreme Greed).

Using historical trade-level data combined with a sentiment index, we evaluate:

📈 Daily PnL distribution

🎯 Win rate across sentiment regimes

⚖️ Long–short positioning bias

📊 Trader segmentation (Volume, Frequency, Consistency)

📉 Risk-adjusted performance (Sharpe proxy)

🔎 Behavioral differences under different market conditions

The objective is to uncover structural patterns in trader profitability, consistency, and risk exposure under changing sentiment environments.

🗂️ Dataset

Two datasets were used:

Fear & Greed Index

Daily market sentiment classification

Categories:

Extreme Fear

Fear

Neutral

Greed

Extreme Greed

Historical Trade Data

Account-level trades

Closed PnL

Trade direction (BUY / SELL)

Execution price & size

Timestamp

The datasets were merged on date to align trades with the prevailing sentiment regime.

🔬 Methodology
1️⃣ Data Processing

Cleaned and validated raw trade data

Converted timestamps to daily frequency

Merged sentiment data on trade dates

2️⃣ Feature Engineering

We created the following trader-level metrics:

Daily account-level PnL

Win rate

Average daily PnL

PnL volatility (standard deviation)

Risk-adjusted return (Sharpe proxy)

3️⃣ Trader Segmentation

Traders were segmented using median-based thresholds:

Volume Segment

High Volume

Low Volume

Frequency Segment

Frequent

Infrequent

Consistency Segment

Low volatility → Consistent

High volatility → Inconsistent

4️⃣ Behavioral Analysis

We analyzed:

Average PnL by sentiment regime

Win rate across sentiment regimes

Long–short ratio (BUY / SELL bias)

Performance by:

Volume segment × Sentiment

Frequency segment × Sentiment

Consistency segment × Sentiment

Outliers in daily PnL were trimmed using the IQR method for distribution clarity.

📊 Key Insights
🔹 1. PnL Distribution

Daily PnL is highly concentrated around zero

Heavy tails indicate episodic large gains/losses

Return distribution is non-normal and fat-tailed

🔹 2. Sentiment & Performance

Performance varies meaningfully across sentiment regimes

Extreme conditions show higher dispersion in profitability

🔹 3. Long–Short Bias

Traders exhibit sentiment-dependent positioning bias

Extreme Greed tends to shift long-short imbalance

🔹 4. Consistency Matters

High raw returns often coincide with high volatility

Risk-adjusted return highlights true efficiency

Consistent traders demonstrate more stable performance

🔹 5. Behavioral Segmentation

Segmenting traders (Volume, Frequency, Consistency) reveals:

Different profitability structures

Different exposure to sentiment shifts

Structural differences in risk-taking behavior

📈 Output Visualizations

Generated charts include:

Daily PnL distribution (Full & Outlier-Removed)

Win rate by sentiment

Long–Short ratio by sentiment

Average PnL by:

Volume segment × Sentiment

Frequency segment × Sentiment

Consistency × Sentiment

All charts are available in the outputs/ folder.

🛠️ Tech Stack

Python

Pandas

NumPy

Matplotlib

▶️ How to Run

Clone the repository:

git clone https://github.com/your-username/primetrade-sentiment-analysis.git
cd primetrade-sentiment-analysis


Install dependencies:

pip install -r requirements.txt


Open the notebook:

jupyter notebook notebooks/analysis.ipynb


Run all cells.

🎯 Business Relevance

This analysis demonstrates:

Behavioral finance principles

Risk-adjusted performance evaluation

Multi-dimensional segmentation analysis

Practical financial data engineering

Structured analytical storytelling

The framework can be extended to:

Strategy backtesting

Alpha factor evaluation

Portfolio risk modeling

Trader profiling & monitoring

🚀 Future Improvements

Add rolling Sharpe ratios

Incorporate drawdown analysis

Build predictive models for regime-based performance

Create interactive dashboards (Plotly / Streamlit)

👤 Author

Pulkit Srivastava
Financial Data & Quantitative Analysis Project
# Stock-Crash-Analysis
.
This project is licensed under the MIT License.<img width="1920" height="1020" alt="Screenshot 2025-11-21 111405" src="https://github.com/user-attachments/assets/ff799271-a48e-4af6-8e2e-4fc872735196" />

📉 Stock Market Crash Analysis with Python

This project performs an in-depth analysis of 30 years of historical Indian stock market (Sensex) data to study the causes, patterns, and indicators of major stock market crashes.
The project also builds an Early Warning System (EWS) to detect potential pre-crash conditions using rolling volatility and return metrics.

📌 Key Objectives

Clean and preprocess long-term stock market time-series data

Identify daily crashes using percentage drops

Detect deep market drawdowns and cluster periods of prolonged stress

Visualize market behaviour before, during, and after crashes

Compare major crash events (1997, 2008–2009, 2020)

Simulate synthetic 2025 data to test an early warning model

Trigger warnings based on rolling mean returns and volatility

📂 Dataset

30+ years of historical Sensex data

Columns include: Date, Open, High, Low, Close, Volume

Synthetic datasets were generated for 2025 crash simulation

🛠️ Technologies Used

Python

Pandas, NumPy

Plotly for interactive visualizations

Datetime & rolling statistics for signal processing

📊 Project Features
✔ 1. Data Preprocessing

Convert dates to datetime format

Sort chronologically

Set Date as index

✔ 2. Daily Crash Detection

Compute daily % returns

Flag days with drop ≥ 5%

✔ 3. Market Drawdown Analysis

Compute cumulative max

Measure drawdown from peak

Identify crashes deeper than 20%

Detect crash clusters using contiguous dates

✔ 4. Crash Period Visualization

Interactive charts for each major crash:

1997 Asian Financial Crisis

2008–2009 Global Financial Crisis

2020 COVID-19 Crash

Charts include:

Closing price

Daily returns

Drawdown curves

✔ 5. Crash Clustering

Group consecutive stress days

Detect clusters lasting weeks/months

Compare duration, depth, and recovery

✔ 6. Early Warning System (EWS)

Pre-crash indicators used:

10-day moving average return < –0.5%

10-day rolling volatility > 2%

Simulated 2025 dataset shows:

Warning signals form before the crash

Volatility spikes ahead of market fall

🚨 Early Warning System Logic
warning_condition = (
    df['Rolling_Mean_Return'] < -0.5
) & (
    df['Rolling_Volatility'] > 2
)


If both conditions hold → Warning Triggered

📈 Example Visualizations

Sensex closing price with crash days highlighted

Drawdown over 30 years (with thresholds)

Crash cluster zoom-in windows (±30 days)

Synthetic 2025 crash with warning markers

All charts are implemented using Plotly, providing interactive sliders and hover-data.

📦 Installation & Setup
1. Clone the repository
git clone https://github.com/yourusername/stock-crash-analysis.git
cd stock-crash-analysis

2. Install dependencies
pip install -r requirements.txt

3. Run the notebook or Python scripts
python analysis.py

📁 Repository Structure
│── data/
│     ├── cleaned_sensex.csv
│     └── synthetic_2025.csv
│
│── notebooks/
│     └── crash_analysis.ipynb
│
│── src/
│     ├── preprocessing.py
│     ├── crash_detection.py
│     ├── clustering.py
│     └── early_warning.py
│
│── README.md
│── requirements.txt
│── LICENSE

💡 Insights Gained

Markets often show increasing volatility before crashes

Drawdowns reveal prolonged stress not visible in daily returns

Major crashes (2008, 2020) show similar pre-pattern dynamics

Early warning indicators can detect deterioration earlier than price charts

📚 Future Improvements

Deploy EWS as a dashboard

Add machine learning models (e.g., LSTM, anomaly detection)

Build a real-time data pipeline

Integrate macro-economic indicators

🤝 Contributing

Pull requests are welcome!
If you have ideas to improve detection algorithms or visualizations, feel free to open an issue.

📜 License




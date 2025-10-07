# 📈 Stock Market Indicator

## 🧠 Project Overview
**Stock Market Indicator** is a Python-based analytical tool that uses **Yahoo Finance data** to identify potential support/resistance zones and evaluate market momentum through the **Relative Strength Index (RSI)** indicator.  
The project visualizes both **price trends** and **RSI movement**, helping investors or analysts make informed trading decisions.

It uses the `yfinance` API to fetch historical data, analyzes price ranges, and calculates common resistance levels using statistical frequency of price occurrences.  
Additionally, RSI is computed using standard 14-day rolling averages to visualize **overbought (70)** and **oversold (30)** regions.

---

## ⚙️ Installation

### 1️⃣ Clone the repository
```bash
git clone https://github.com/<your-username>/StockMarketIndicator.git
2️⃣ Navigate to the project directory
bash
Copy code
cd StockMarketIndicator
3️⃣ Install dependencies
Make sure you have Python 3.8+ installed, then install required packages:

bash
Copy code
pip install yfinance matplotlib numpy
📦 Requirements
Python ≥ 3.8

Libraries:

yfinance

matplotlib

numpy

collections

datetime

You can also install everything from a requirements.txt file if provided:

bash
Copy code
pip install -r requirements.txt
🚀 Usage
Run the script directly:
bash
Copy code
python stock_market_indicator.py
The script will:

Fetch 2 years of historical stock data (default: LICI.NS).

Calculate the maximum, minimum, and frequent price levels.

Compute RSI (Relative Strength Index) using a 14-day moving average.

Plot:

Stock closing prices

RSI levels

Support/resistance bands for the top 10 frequent price levels

📊 Example Output
After running the script, a window opens showing:

A line chart of stock prices with horizontal blue bars (support/resistance levels).

A second chart displaying RSI with buy (green) and sell (red) threshold lines.

text
Copy code
Top 10 frequent price levels: 
1234.0, 1238.0, 1242.0, 1247.0, 1250.0, 1253.0, 1256.0, 1260.0, 1264.0, 1268.0
🧮 Core Logic Breakdown
Data Retrieval:

python
Copy code
import yfinance
symb = yfinance.Ticker('LICI.NS')
hist = symb.history(period='2y')
Price Analysis:

Finds highest and lowest stock prices.

Identifies most frequent price levels using collections.Counter.

RSI Calculation:

Uses daily price changes.

Separates positive and negative differences.

Computes 14-period averages and RSI formula:

𝑅
𝑆
𝐼
=
100
×
𝐴
𝑣
𝑔
_
𝑈
𝑝
𝐴
𝑣
𝑔
_
𝑈
𝑝
+
𝐴
𝑣
𝑔
_
𝐷
𝑜
𝑤
𝑛
RSI=100× 
Avg_Up+Avg_Down
Avg_Up
​
 
Visualization:

Plots both stock price trends and RSI chart using matplotlib.

Highlights overbought (70) and oversold (30) zones.

Displays major resistance levels on the price chart.

💡 Future Enhancements
Add a GUI dashboard using Tkinter or Streamlit.

Support multiple tickers dynamically.

Integrate moving averages or Bollinger Bands for deeper analysis.

Export data/plots to .csv and .png formats automatically.

👨‍💻 Author
Ujjawal Yadav
Python Developer | Data & Finance Enthusiast
📧 [Your Email Here]
🌐 [Your GitHub Profile Link Here]

🪪 License
This project is licensed under the MIT License — free for modification and distribution with attribution.

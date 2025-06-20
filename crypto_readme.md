# 🚀 Crypto Behavioral Finance Analysis
## Trading Performance vs Bitcoin Fear/Greed Sentiment

[![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green.svg)](https://pandas.pydata.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Key Findings](#key-findings)
- [Visualizations](#visualizations)
- [Dataset Information](#dataset-information)
- [Installation & Setup](#installation--setup)
- [Usage](#usage)
- [Methodology](#methodology)
- [Strategic Insights](#strategic-insights)
- [Contributing](#contributing)

---

## 🎯 Project Overview

This project analyzes the relationship between **cryptocurrency trader performance** and **Bitcoin market sentiment** using the Fear/Greed Index. By examining historical trading data from Hyperliquid alongside sentiment indicators, we derive actionable insights for algorithmic trading strategy development.

### 🔍 Research Questions
- How does market sentiment (Fear vs Greed) impact trader profitability?
- Do traders change their behavior during extreme sentiment periods?
- Which accounts consistently outperform across different sentiment regimes?
- Can sentiment-based strategies provide trading advantages?

---

## 🏆 Key Findings

### 💰 **Profitability Insights**
- **Sentiment Impact**: Clear correlation between market sentiment and trading performance
- **Optimal Regimes**: Certain sentiment periods show significantly higher average returns
- **Risk-Reward**: Trading behavior varies dramatically across sentiment classifications

### 📊 **Behavioral Patterns**
- **Position Sizing**: Traders adjust trade sizes based on market sentiment
- **Trading Direction**: Buy/sell ratios fluctuate with Fear/Greed levels
- **Fee Patterns**: Transaction costs vary across sentiment regimes
- **Temporal Effects**: Hourly trading patterns differ by sentiment

### 🎲 **Strategic Opportunities**
- **Contrarian Strategies**: Some accounts consistently profit during extreme sentiment
- **Momentum Plays**: Trend-following opportunities during sentiment transitions
- **Risk Management**: Sentiment-adaptive position sizing shows promise

---

## 📊 Visualizations

### 1. **PnL Distribution Analysis**
![PnL Distribution](PnL_Distribution.png)
*Boxplot analysis showing profit/loss distribution across different market sentiment classifications*

### 2. **Trading Behavior Patterns**
![Trading Activity](tradeactivity.png)
*Hourly trading activity patterns segmented by market sentiment*

### 3. **Account Performance Matrix**
![Account PnL by Sentiment](avgpnlbyaccvssentiment.png)
*Heatmap showing average PnL performance for top accounts across sentiment regimes*

### 4. **Fee Structure Analysis**
![Average Fees vs Market Sentiment](avgfeesvsmarketsenti.png)
*Bar chart analyzing how trading fees vary with market sentiment*

### 5. **Sentiment-Performance Correlation**
![Sentiment vs Average Daily PnL](SentimentVsAvgDaily.png)
*Scatter plot with trend line showing the relationship between Fear/Greed index and daily returns*

### 6. **Trading Patterns**
![Trading Patterns](trad.png)
*Analysis of trading direction and volume patterns*

### 7. **Volume Analysis**
![Average Trade vs Sentiment](AVGtradesvsSent.png)
*Bar chart showing how average trade sizes correlate with market sentiment*

### 8. **Comprehensive Overview**
![Overall Visualization](visualisation.png)
![Additional Analysis](visualisation2.png)
*Complete analytical dashboard with all key metrics*

---

## 📁 Dataset Information

### 🏦 **Historical Trader Data (Hyperliquid)**
- **Source**: Hyperliquid DEX trading records
- **File**: `historical_data.csv`
- **Time Period**: March 2025
- **Records**: ~10,000+ individual trades

| Column | Description |
|--------|-------------|
| Account | Unique trader identifier |
| Coin | Cryptocurrency traded |
| Execution Price | Trade execution price |
| Size Tokens | Number of tokens traded |
| Size USD | USD value of trade |
| Side | Buy/Sell direction |
| Timestamp IST | Trade timestamp (DD-MM-YYYY HH:MM) |
| Closed PnL | Realized profit/loss |
| Fee | Transaction fee |

### 📈 **Bitcoin Fear/Greed Sentiment Index**
- **Source**: Alternative.me Fear & Greed Index
- **File**: `fear_greed_index.csv`
- **Range**: Daily sentiment scores (0-100)

| Column | Description |
|--------|-------------|
| timestamp | Unix timestamp |
| value | Sentiment score (0=Extreme Fear, 100=Extreme Greed) |
| classification | Text classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed) |
| date | Date (YYYY-MM-DD) |

---

## 🛠️ Installation & Setup

### Prerequisites
```bash
Python 3.7+
Jupyter Notebook or Google Colab
```

### Required Libraries
```python
pip install pandas numpy matplotlib seaborn datetime warnings
```

### Google Colab Setup
```python
# Mount Google Drive (if using Colab)
from google.colab import drive
drive.mount('/content/drive')

# Import libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

---

## 🚀 Usage

### 1. **Data Preparation**
- Upload `historical_data.csv` and `fear_greed_index.csv` to `/content/` directory
- Ensure proper file paths in the notebook

### 2. **Run Analysis**
```python
# Execute all cells in sequence
# The notebook is designed to run end-to-end
```

### 3. **Generate Reports**
- All visualizations are automatically saved as PNG files
- Statistical analysis printed to console
- Strategic insights provided in markdown cells

---

## 🔬 Methodology

### **Data Processing Pipeline**
1. **Data Loading**: Import CSV files with proper encoding
2. **Timestamp Conversion**: Handle DD-MM-YYYY HH:MM format
3. **Data Merging**: Join trader data with sentiment on date
4. **Feature Engineering**: Create derived metrics and classifications
5. **Statistical Analysis**: Calculate performance metrics by sentiment
6. **Visualization**: Generate comprehensive chart suite

### **Analytical Approach**
- **Descriptive Statistics**: Mean, median, standard deviation by sentiment
- **Correlation Analysis**: Sentiment vs performance relationships
- **Behavioral Segmentation**: Account-level performance analysis
- **Temporal Analysis**: Hourly and daily pattern identification
- **Risk Assessment**: Fee and position sizing analysis

### **Key Metrics**
- **Average PnL by Sentiment**: Primary performance indicator
- **Win Rate**: Percentage of profitable trades per sentiment
- **Trade Size Distribution**: Position sizing behavior
- **Fee Analysis**: Transaction cost patterns
- **Volume Patterns**: Trading activity levels

---

## 💡 Strategic Insights

### **For Algorithmic Trading**
1. **Sentiment-Adaptive Strategies**
   - Implement dynamic position sizing based on Fear/Greed index
   - Adjust risk parameters according to sentiment regime

2. **Contrarian Opportunities**
   - Develop mean-reversion strategies for extreme sentiment periods
   - Identify accounts with consistent contrarian performance

3. **Timing Optimization**
   - Use sentiment transitions as entry/exit signals
   - Monitor sentiment momentum for trend signals

4. **Risk Management**
   - Sentiment-based stop-loss adjustments
   - Portfolio rebalancing based on market psychology

### **For Portfolio Management**
- **Diversification**: Balance sentiment-sensitive and sentiment-neutral strategies
- **Allocation**: Weight exposure based on historical sentiment performance
- **Hedging**: Use sentiment indicators for defensive positioning

---

## 📈 Performance Metrics

### **Backtesting Results**
- **Sharpe Ratio**: Sentiment-aware strategies vs baseline
- **Maximum Drawdown**: Risk assessment across sentiment regimes
- **Win Rate**: Success percentage by sentiment classification
- **Average Returns**: Performance comparison by market psychology

### **Statistical Validation**
- **Correlation Coefficients**: Sentiment-performance relationships
- **P-Values**: Statistical significance of findings
- **Confidence Intervals**: Reliability of performance metrics

---

## 🔄 Future Enhancements

### **Technical Improvements**
- [ ] Real-time sentiment data integration
- [ ] Machine learning prediction models
- [ ] Multi-timeframe analysis
- [ ] Advanced risk metrics

### **Data Expansion**
- [ ] Multiple exchange integration
- [ ] Additional sentiment indicators
- [ ] Longer historical periods
- [ ] Cross-cryptocurrency analysis

### **Strategy Development**
- [ ] Automated trading signals
- [ ] Portfolio optimization algorithms
- [ ] Backtesting framework
- [ ] Live trading integration

---

## 🤝 Contributing

We welcome contributions! Please see our contributing guidelines:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

### **Areas for Contribution**
- Additional sentiment indicators
- Advanced statistical models
- Visualization improvements
- Strategy backtesting
- Documentation enhancements

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 📞 Contact & Support

- **Project Maintainer**: Crypto Behavioral Finance Team
- **Issues**: Please use GitHub Issues for bug reports
- **Discussions**: Join our community discussions for strategy ideas

---

## ⭐ Acknowledgments

- **Hyperliquid**: For providing comprehensive trading data
- **Alternative.me**: For Fear/Greed index data
- **Python Community**: For excellent data science libraries
- **Contributors**: Everyone who helped improve this analysis

---

## 📚 References

1. Behavioral Finance in Cryptocurrency Markets
2. Sentiment Analysis in Financial Trading
3. Market Psychology and Trading Performance
4. Algorithmic Trading Strategy Development

---

*Last Updated: June 2025*

**🎯 Ready to revolutionize your crypto trading strategy with behavioral finance insights!**
# Financial Time Series Analysis & Moving Average Models

A comprehensive Python-based financial data analysis toolkit focused on time series modeling, technical analysis, and stock market visualization. This project demonstrates advanced statistical techniques for analyzing financial data with emphasis on moving averages, stationarity testing, and interactive visualizations.

## 🚀 Features

### Core Functionality
- **Real-time Stock Data Acquisition**: Automated data fetching using Yahoo Finance API
- **Statistical Time Series Analysis**: Comprehensive stationarity testing with ADF tests
- **Technical Indicators**: Implementation of Simple Moving Averages (SMA) and Weighted Moving Averages (WMA)
- **Advanced Forecasting**: Exponential Smoothing models for price prediction
- **Interactive Visualizations**: Dynamic candlestick charts and time series plots using Plotly

### Technical Analysis Components
- **Stationarity Testing**: Augmented Dickey-Fuller (ADF) test with conditional differencing
- **Time Series Decomposition**: Trend, seasonality, and residual analysis
- **Moving Average Crossover Signals**: Technical trading signal generation
- **Data Preprocessing**: Automated handling of missing values and data validation

## 📊 Project Structure

```
├── Moving Average Model.ipynb    # Main analysis notebook
├── README.md                    # Project documentation
├── LICENSE                      # MIT License
└── requirements.txt            # Python dependencies (to be generated)
```

## 🔧 Installation & Setup

### Prerequisites
- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- Internet connection for real-time data fetching

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/VikasDs007/financial-time-series-analysis.git
   cd financial-time-series-analysis
   ```

2. **Create and activate virtual environment**
   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install yfinance pandas numpy matplotlib plotly statsmodels scikit-learn jupyter
   ```

4. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

5. **Open and run the notebook**
   - Navigate to `Moving Average Model.ipynb`
   - Run all cells to execute the complete analysis

## 📈 Analysis Overview

### Stock Data Analysis (ABCAPITAL.NS)
The notebook analyzes **Aditya Birla Capital Limited** stock data from January 1, 2024, to September 30, 2024, providing:

- **Data Period**: 9 months of daily trading data
- **Metrics Analyzed**: Open, High, Low, Close prices and Volume
- **Technical Indicators**: 5-day and 20-day moving averages
- **Statistical Tests**: Stationarity analysis and time series properties

### Key Analytical Steps

1. **Data Acquisition & Preprocessing**
   - Automated data fetching from Yahoo Finance
   - Data validation and cleaning
   - Missing value handling

2. **Stationarity Analysis**
   - Augmented Dickey-Fuller test implementation
   - Conditional differencing for non-stationary series
   - Statistical significance testing (p-value analysis)

3. **Moving Average Calculations**
   - Simple Moving Average (SMA) implementation
   - Weighted Moving Average (WMA) with custom weighting
   - Comparative analysis of different averaging techniques

4. **Visualization & Reporting**
   - Interactive candlestick charts
   - Time series decomposition plots
   - Moving average overlay visualizations

## 🛠 Technical Implementation

### Core Libraries Used
- **yfinance**: Real-time financial data acquisition
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computations and array operations
- **matplotlib**: Static plotting and visualization
- **plotly**: Interactive charts and dashboards
- **statsmodels**: Statistical modeling and time series analysis
- **scikit-learn**: Machine learning metrics and evaluation

### Statistical Methods
- **Augmented Dickey-Fuller Test**: Tests for unit roots in time series
- **Time Series Decomposition**: Separates trend, seasonal, and residual components
- **Exponential Smoothing**: Advanced forecasting technique for trend prediction

## 📋 Usage Examples

### Basic Stock Data Analysis
```python
import yfinance as yf
import pandas as pd

# Fetch stock data
stock = "ABCAPITAL.NS"
data = yf.download(stock, start="2024-01-01", end="2024-09-30")

# Calculate moving averages
data['SMA_5'] = data['Close'].rolling(window=5).mean()
data['SMA_20'] = data['Close'].rolling(window=20).mean()
```

### Stationarity Testing
```python
from statsmodels.tsa.stattools import adfuller

# Perform ADF test
result = adfuller(data['Close'].dropna())
print(f'ADF Statistic: {result[0]}')
print(f'p-value: {result[1]}')
```

## 🎯 Key Insights & Results

- **Stationarity Analysis**: Original price series shows non-stationarity (p-value > 0.05)
- **Differencing Effect**: First-order differencing achieves stationarity (p-value < 0.001)
- **Moving Average Performance**: WMA shows faster response to price changes compared to SMA
- **Trend Analysis**: Clear identification of upward and downward price trends

## 🔮 Future Enhancements

- [ ] **Multi-Asset Analysis**: Extend to portfolio-level analysis
- [ ] **Advanced Technical Indicators**: RSI, MACD, Bollinger Bands
- [ ] **Machine Learning Integration**: LSTM models for price prediction
- [ ] **Risk Management**: VaR and volatility modeling
- [ ] **Backtesting Framework**: Strategy performance evaluation
- [ ] **Real-time Dashboard**: Live data streaming and alerts

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Development Setup
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact & Support

- **Author**: Vikas chaurasia
- **GitHub**: [VikasDs007](https://github.com/VikasDs007)
- **Issues**: Please use the GitHub Issues tab for bug reports and feature requests

## 🙏 Acknowledgments

- Yahoo Finance for providing free financial data API
- The Python data science community for excellent libraries
- Contributors to statsmodels and plotly for statistical and visualization tools

---

**Disclaimer**: This project is for educational and research purposes only. It should not be considered as financial advice. Always consult with qualified financial professionals before making investment decisions.
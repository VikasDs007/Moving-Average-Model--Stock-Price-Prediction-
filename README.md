# Data Analysis and Time Series Modeling

This repository contains Jupyter Notebooks exploring data visualization techniques and time series forecasting models.

## Projects Included:

### 1. Data Visualization Project (`Data Visualization.ipynb`)

* **Description:** This notebook focuses on visualizing data, likely involving an analysis of population trends from 1955-2020. It utilizes Python libraries such as Pandas for data manipulation and Matplotlib/Seaborn for plotting. It also demonstrates exporting data to an Excel file.
* **Key Features:**
    * Data loading and cleaning.
    * Line plots for population trends.
    * Exporting pivot tables to Excel.
* **Outputs:** `my_test.png`, `pivot_table.xlsx` (if included in repo)

### 2. Moving Average Model for Stock Data Analysis (`Moving Average Model.ipynb`)

* **Description:** This notebook provides a comprehensive guide to building and evaluating a Moving Average Model using **real-time stock data for ABCAPITAL.NS (from 2024-01-01 to 2024-09-30)**. It covers data acquisition, calculation of Simple Moving Averages (SMA) and Weighted Moving Averages (WMA), **time series stationarity checks with conditional differencing**, time series decomposition, and interactive Plotly charts for visualization.
* **Key Features:**
    * Real-time stock data acquisition via `yfinance`.
    * **Stationarity testing (ADF test) and conditional differencing.**
    * Calculation and visualization of SMA and WMA.
    * Time series decomposition (trend, seasonality, residuals).
    * Interactive candlestick charts with Plotly.
    * Exponential Smoothing model forecasting.
* **Outputs:** `irfc_candlestick_chart.html` (consider renaming this to `abcapital_candlestick_chart.html` or a more generic name if the ticker can change, and adding `exponential_smoothing_forecast.html` if you save that plot as HTML).

## How to Run the Notebooks

To run these notebooks locally, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone <your-repository-url>
    cd <your-repository-name>
    ```
2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    # On Windows
    .\venv\Scripts\activate
    # On macOS/Linux
    source venv/bin/activate
    ```
3.  **Install the required libraries:**
    Generate a `requirements.txt` file by running `pip freeze > requirements.txt` after installing all necessary libraries.
    ```bash
    pip install -r requirements.txt
    ```
4.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
5.  Open the desired notebook (`Data Visualization.ipynb` or `Moving Average Model.ipynb`) in your browser and run the cells.

## Dependencies

All required Python libraries are listed in `requirements.txt`. Key libraries include:

* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `yfinance`
* `plotly`
* `statsmodels`
* `openpyxl`

## License

[Specify your license here, e.g., MIT License]
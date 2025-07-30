# nse-volatility-tracker
# Tracking Stock Market Volatility: The 2025 Tariff Impact on NSE Indices

## Overview
This project is a Jupyter notebook that fetches historical data for NSE indices, calculates rolling 30-day annualized volatility, and visualizes it using Plotly. It aims to monitor volatility changes, with a focus on potential impacts from 2025 tariffs. Indices tracked: NIFTY AUTO, BANK, ENERGY, FMCG, IT, MEDIA, METAL, PHARMA, REALTY.

Key features:
- Fetches index data using custom NSE utilities.
- Computes daily returns and rolling volatility (std * sqrt(252)).
- Generates an interactive line plot of volatility over time.
- Data period: From Dec 31, 2024, to Jun 6, 2025 (adjustable).

## Requirements
- Python 3.8+
- Libraries: 
  - pandas
  - numpy
  - plotly
  - IPython (for display)
  - Custom: NseUtility, NseHistorical (ensure these modules are available or install equivalents)

Install core dependencies:
pip install pandas numpy plotly ipython

Note: Custom NSE modules (NseUtility, NSEMasterData) may need to be sourced or replaced with alternatives like nsepy for data fetching.

1. Clone the repository:
git clone https://github.com/keshi-17/nse-volatility-tracker.git
cd nse-volatility-tracker

2. Ensure NSE data utilities are set up (e.g., download symbol master).

3. Open the Jupyter notebook:
jupyter notebook TrumpTariffimpact.ipynb

4. Run the cells sequentially:
- Cells 1-2: Import libraries and fetch closing prices for indices.
- Cells 3-6: Create DataFrame, calculate returns, rolling volatility, and drop NaNs.
- Cell 9: Plot volatility (saves `volatility_plot.png` and displays it).

Outputs include DataFrames of prices/volatility and a Plotly figure saved as an image.

## Data Sources
- Historical data from NSE via custom utilities.
- Adjust start/end dates in code for different periods.

## Limitations
- Dependent on custom NSE modules; may require API keys or alternatives.
- Volatility calculation assumes 252 trading days per year.
- Plot is for visualization; no statistical tests included.

## License
MIT License. Feel free to use and modify.

# MercadoLibre Search Traffic and Stock Price Analysis

## Project Overview

This project investigates the relationship between MercadoLibre's Google search traffic and its stock price behavior. As a growth analyst for MercadoLibre, with over 200 million users in Latin America, you aim to uncover insights that may help predict search traffic trends and explore if these insights can translate into successful stock trading strategies.

The analysis is divided into four key steps:
1. Identifying unusual patterns in hourly Google search traffic.
2. Mining the search traffic data for seasonal trends.
3. Relating search traffic to stock price patterns.
4. Creating a time series model using Prophet to forecast search traffic.

## Background

E-commerce platforms like MercadoLibre faced significant challenges during the global financial disruptions of 2020. However, many platforms saw new customer growth and increased revenues after an initial period of shock. By analyzing search traffic and stock price patterns, this project seeks to uncover actionable insights for the company's growth.

## Instructions

### Step 1: Find Unusual Patterns in Hourly Google Search Traffic
To determine if search traffic is linked to financial events or if it simply represents random noise:
- Analyze hourly search data for May 2020, the month of MercadoLibre's quarterly financial results release.
- Visualize and compare the total search traffic for May 2020 against the monthly median across all months.
- Answer the question: Did search traffic increase during the release of the financial results?

### Step 2: Mine the Search Traffic Data for Seasonality
To help the marketing team focus efforts at peak times:
- Group hourly search data by the hour of day and analyze traffic peaks during the day.
- Group hourly search data by the day of the week to determine the busiest day.
- Group hourly search data by the week of the year to examine if search traffic increases during the winter holiday season (weeks 40–52).
- Identify any time-based seasonal trends.

### Step 3: Relate the Search Traffic to Stock Price Patterns
To investigate the relationship between search data and stock price patterns:
- Read and plot stock price data, and merge it with the search traffic data.
- Slice the data to focus on the first half of 2020 (January to June) and visualize if both time series show trends consistent with e-commerce growth during this period.
- Add derived columns to the DataFrame:
  - `Lagged Search Trends`: Shifts search traffic by one hour.
  - `Stock Volatility`: Exponentially weighted four-hour rolling average of stock volatility.
  - `Hourly Stock Return`: Percent change in stock price on an hourly basis.
- Analyze the correlation between lagged search traffic, stock volatility, and hourly stock returns.

### Step 4: Create a Time Series Model with Prophet
To analyze and forecast search traffic patterns:
- Set up a Prophet model with the Google search traffic data.
- Plot the model's forecast to examine the near-term popularity of MercadoLibre.
- Break down the time series components to answer:
  - Which time of day exhibits the greatest popularity?
  - Which day of the week sees the highest search traffic?
  - What is the lowest search traffic point in the calendar year?

## Results and Insights

- **Unusual Patterns**: Google search traffic during May 2020 indicated potential spikes tied to the financial results announcement.
- **Seasonality**: Search traffic showed daily and weekly patterns, with peaks at certain hours of the day and days of the week.
- **Search and Stock Relationships**: While stock price trends aligned with the recovery narrative for e-commerce in 2020, search traffic exhibited volatility, and the correlation between lagged search traffic and stock metrics was weak.
- **Forecasting**: The Prophet model provided insights into future search trends, highlighting high-traffic periods and seasonal dips.

## Datasets
The following datasets are used in this project:
- [Mercado Google Hourly Search Trends](https://static.bc-edx.com/ai/ail-v-1-0/m8/lms/datasets/google_hourly_search_trends.csv)
- [Mercado Stock Prices](https://static.bc-edx.com/ai/ail-v-1-0/m8/lms/datasets/mercado_stock_price.csv)

## Technologies and Tools
- **Python Libraries**:
  - `pandas` for data manipulation and analysis
  - `matplotlib` for data visualization
  - `fbprophet` for time series forecasting
- **Environment**:
  - Jupyter Notebook for running the analysis

## Usage
1. Clone the repository to your local machine.
2. Download the datasets linked above and place them in the same directory as the notebook.
3. Install the required Python libraries using `pip install -r requirements.txt`.
4. Open the Jupyter Notebook and run the cells to replicate the analysis.



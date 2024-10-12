# Cryptocurrency Price Tracking and Analysis

## Project Overview
This project tracks and analyzes the latest cryptocurrency data from the CoinMarketCap API. It gathers information about the top 15 cryptocurrencies by market capitalization and updates this data at regular intervals, saving it into a CSV file for further analysis. The project uses Python with various libraries to request the API, process and normalize the JSON data, and analyze trends in price and percentage changes over time.

## Features
- **API Integration**: Connects to the CoinMarketCap API to retrieve real-time data for the top 15 cryptocurrencies in terms of market capitalization.
- **Data Collection**: Retrieves cryptocurrency data, including price, market cap, volume, and percentage changes for various time periods (1 hour, 24 hours, 7 days, etc.).
- **Scheduled Data Collection**: Automates the data collection process at 1-minute intervals for a set duration (333 iterations) to store the data over time in a CSV file.
- **Data Storage**: Appends new data entries to a CSV file, enabling easy retrieval and long-term tracking of cryptocurrency trends.
- **Data Analysis**: Uses Pandas to normalize JSON responses, analyze data, and calculate average percentage changes across different time periods for each cryptocurrency.
- **Visualization**: Implements Seaborn to create visualizations that display trends in price changes over various time periods for each cryptocurrency.

## Key Data Points
- **Name**: Name of the cryptocurrency (e.g., Bitcoin, Ethereum)
- **Price**: The current price in USD.
- **Market Cap**: The total market capitalization.
- **Volume**: 24-hour trading volume.
- **Percentage Change**: Price changes over different periods (1 hour, 24 hours, 7 days, 30 days, 60 days, and 90 days).

## Technologies Used
- **Python**: Core programming language.
- **Pandas**: Data manipulation and analysis.
- **Requests**: API requests and session management.
- **JSON**: For parsing and handling API responses.
- **Seaborn & Matplotlib**: For data visualization and creating graphs.
- **CoinMarketCap API**: To gather real-time cryptocurrency data.

## How It Works
1. **API Requests**: The project sends API requests to the CoinMarketCap API using a session that includes an API key for authentication.
2. **Data Processing**: The response is processed, and the relevant fields (price, market cap, percentage changes, etc.) are extracted and normalized into a Pandas DataFrame.
3. **Scheduled Data Updates**: The `api_runner()` function runs at 1-minute intervals to fetch and append data to the CSV file over time.
4. **Data Analysis**: The project groups and analyzes the percentage changes for various cryptocurrencies over multiple time periods and averages them to gain insights into price movements.
5. **Visualization**: Finally, the project creates point plots using Seaborn to visualize the price percentage changes for different cryptocurrencies.

## Output
- A CSV file containing the historical data of cryptocurrencies, including price, market cap, and percentage changes.
- Visualizations showing trends in cryptocurrency price movements.

## Requirements
- Python 3.x
- Pandas
- Requests
- Seaborn
- Matplotlib
- CoinMarketCap API Key

## Future Improvements
- Add support for more cryptocurrencies and metrics.
- Implement a real-time dashboard for continuous monitoring.
- Explore machine learning models for predicting price movements.

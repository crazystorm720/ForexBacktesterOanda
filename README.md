# ForexBacktesterOanda

## Project Overview

ForexBacktesterOanda is a Python-based project that facilitates the backtesting of forex trading strategies using historical data from the Oanda API. The project focuses on fetching and storing forex data in an SQLite database and provides a framework for implementing and evaluating various trading strategies.

## Key Features

- Fetches historical forex data from the Oanda API for a specified instrument, granularity, and date range.
- Stores the fetched data in an SQLite database for efficient access and management.
- Implements a modular and reusable design, separating data ingestion, database operations, and backtesting logic.
- Provides a flexible framework for defining and backtesting trading strategies.
- Includes error handling and data validation to ensure data integrity and reliability.
- Utilizes parameterized queries to prevent SQL injection vulnerabilities.
- Offers command-line arguments for easy configuration and customization of data ingestion parameters.

## Prerequisites

Before running the project, ensure that you have the following prerequisites installed:

- Python 3.7 or higher
- Oanda API key (sign up at [Oanda](https://www.oanda.com/) to obtain an API key)

## Installation

1. Clone the repository:

```shell
git clone https://github.com/your-username/ForexBacktesterOanda.git
```

2. Navigate to the project directory:

```shell
cd ForexBacktesterOanda
```

3. Create a virtual environment (optional but recommended):

```shell
python -m venv venv
source venv/bin/activate
```

4. Install the required dependencies:

```shell
pip install -r requirements.txt
```

## Configuration

1. Create a `config` directory in the project root:

```shell
mkdir config
```

2. Create a `keys.py` file inside the `config` directory:

```shell
touch config/keys.py
```

3. Open the `keys.py` file and add your Oanda API key:

```python
OANDA_API_KEY = 'YOUR_OANDA_API_KEY'
```

Replace `'YOUR_OANDA_API_KEY'` with your actual Oanda API key.

## Usage

To fetch historical forex data and store it in the database, run the following command:

```shell
python src/data/data_ingestion.py --instrument EUR_USD --granularity H1 --days 180
```

This command fetches historical data for the EUR/USD instrument with an hourly granularity (H1) for the last 180 days and stores it in the SQLite database.

You can customize the instrument, granularity, and date range by modifying the command-line arguments.

## Backtesting

To backtest a trading strategy, follow these steps:

1. Implement your trading strategy in the `src/strategies` directory, following the provided template.

2. Update the `src/backtester/backtester.py` file to include your trading strategy and specify the desired backtesting parameters.

3. Run the backtester:

```shell
python src/backtester/backtester.py
```

The backtester will execute your trading strategy on the historical data stored in the database and generate performance metrics and visualizations.

## Testing

To run the test suite, execute the following command:

```shell
pytest tests/
```

This will run all the test cases defined in the `tests/` directory and provide a report of the test results.

## Contributing

Contributions to the ForexBacktesterOanda project are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request on the GitHub repository.

When contributing, please adhere to the existing code style and follow the project's guidelines for commit messages and pull request descriptions.

## License

This project is licensed under the [MIT License](LICENSE).

## Disclaimer

Forex trading involves substantial risk, and past performance is not indicative of future results. The ForexBacktesterOanda project is provided for educational and informational purposes only. It is not intended as financial advice or a recommendation to engage in forex trading. Always consult with a qualified financial professional before making any trading decisions.

## Contact

If you have any questions or inquiries about the ForexBacktesterOanda project, please contact the project maintainer.

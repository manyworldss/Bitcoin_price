# Bitcoin Price Tracker Discord Bot

A Discord bot that tracks Bitcoin prices using the CoinMarketCap API and sends regular updates and price alerts to designated Discord channels.

## Features

- Hourly Bitcoin price updates
- Customizable price alerts for when Bitcoin crosses specified thresholds
- Price history tracking and storage
- Detailed logging system
- Configurable through JSON file

## Setup ##

1. Create a `config.json` file with the following structure:
```json
{
    "cmc_api_key": "your_coinmarketcap_api_key",
    "price_alerts": {
        "above": 50000,
        "below": 40000
    }
}
```

2. Install required dependencies:
```bash
pip install requests discord.py
```

3. Add the bot to your Discord server and create a channel named `bitcoin-alerts`

## Usage

1. Run the bot:
```bash
python bitcoin_tracker.py
```

2. The bot will automatically:
   - Post hourly updates in the `#bitcoin-alerts` channel
   - Send alerts when Bitcoin price crosses configured thresholds
   - Store price history in `price_history.json`
   - Log activities in `bitcoin_tracker.log`

## Monitoring

- Check `bitcoin_tracker.log` for detailed operation logs
- View price history in `price_history.json`
- Monitor updates in the Discord `#bitcoin-alerts` channel

## Note

Make sure to keep your CoinMarketCap API key and Discord bot token secure and never share them publicly.

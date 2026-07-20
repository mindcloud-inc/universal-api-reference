# <img src="https://images.mindcloud.co/apps/icons/coin-market-cap_1775845455408.png" alt="CoinMarketCap logo" width="28" height="28"> CoinMarketCap: Universal API

Access CoinMarketCap Pro market, cryptocurrency, exchange, and sentiment data through the official REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/coinMarketCap/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://coinmarketcap.com
- **Vendor API docs:** https://coinmarketcap.com/api/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Key Info](actions/get-api-key-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-api-key-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Get API Key Info](actions/get-api-key-info.md) | GET | Retrieves API key usage and plan details from CoinMarketCap. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Cryptocurrency Categories](actions/get-cryptocurrency-categories.md) | GET | Retrieves cryptocurrency categories from CoinMarketCap. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Exchange Map](actions/get-exchange-map.md) | GET | Retrieves exchange IDs and slugs from CoinMarketCap. |
| [Get Exchange Market Pairs](actions/get-exchange-market-pairs.md) | GET | Retrieves exchange market pairs from CoinMarketCap. |
| [Get Latest Exchange Listings](actions/get-latest-exchange-listings.md) | GET | Retrieves latest exchange listings from CoinMarketCap. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Cryptocurrency Gainers and Losers](actions/get-cryptocurrency-gainers-and-losers.md) | GET | Retrieves cryptocurrency gainers and losers from CoinMarketCap. |
| [Get Cryptocurrency Info](actions/get-cryptocurrency-info.md) | GET | Retrieves cryptocurrency metadata from CoinMarketCap. |
| [Get Cryptocurrency Map](actions/get-cryptocurrency-map.md) | GET | Retrieves cryptocurrency IDs and symbols from CoinMarketCap. |
| [Get Cryptocurrency Market Pairs](actions/get-cryptocurrency-market-pairs.md) | GET | Retrieves cryptocurrency market pairs from CoinMarketCap. |
| [Get Latest Cryptocurrency Listings](actions/get-latest-cryptocurrency-listings.md) | GET | Retrieves latest cryptocurrency listings from CoinMarketCap. |
| [Get Latest Trending Cryptocurrencies](actions/get-latest-trending-cryptocurrencies.md) | GET | Retrieves latest trending cryptocurrencies from CoinMarketCap. |
| [Get Most Visited Cryptocurrencies](actions/get-most-visited-cryptocurrencies.md) | GET | Retrieves most visited cryptocurrencies from CoinMarketCap. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Cryptocurrency Price Performance Stats](actions/get-cryptocurrency-price-performance-stats.md) | GET | Retrieves cryptocurrency price performance stats from CoinMarketCap. |
| [Get Historical CMC100 Index](actions/get-historical-cmc100-index.md) | GET | Retrieves historical CMC100 index values from CoinMarketCap. |
| [Get Historical Fear and Greed Index](actions/get-historical-fear-and-greed-index.md) | GET | Retrieves historical fear and greed index values from CoinMarketCap. |
| [Get Historical Global Metrics](actions/get-historical-global-metrics.md) | GET | Retrieves historical global crypto market metrics from CoinMarketCap. |
| [Get Latest CMC100 Index](actions/get-latest-cmc100-index.md) | GET | Retrieves the latest CMC100 index value from CoinMarketCap. |
| [Get Latest Fear and Greed Index](actions/get-latest-fear-and-greed-index.md) | GET | Retrieves the latest fear and greed index from CoinMarketCap. |
| [Get Latest Global Metrics](actions/get-latest-global-metrics.md) | GET | Retrieves latest global crypto market metrics from CoinMarketCap. |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [Convert Price](actions/convert-price.md) | GET | Converts amounts between currencies using CoinMarketCap pricing. |
| [Get Historical Cryptocurrency OHLCV](actions/get-historical-cryptocurrency-ohlcv.md) | GET | Retrieves historical cryptocurrency OHLCV data from CoinMarketCap. |
| [Get Historical Cryptocurrency Quotes](actions/get-historical-cryptocurrency-quotes.md) | GET | Retrieves historical cryptocurrency quotes from CoinMarketCap. |
| [Get Latest Cryptocurrency OHLCV](actions/get-latest-cryptocurrency-ohlcv.md) | GET | Retrieves latest cryptocurrency OHLCV data from CoinMarketCap. |
| [Get Latest Cryptocurrency Quotes](actions/get-latest-cryptocurrency-quotes.md) | GET | Retrieves latest cryptocurrency quotes from CoinMarketCap. |


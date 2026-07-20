# CoinMarketCap: Native API Reference

A consolidated summary of CoinMarketCap's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://coinmarketcap.com/api/documentation/
- **API base URL:** `https://pro-api.coinmarketcap.com`

## Authentication

### API Key

Connect with your CoinMarketCap Pro API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://coinmarketcap.com/api/documentation/guides/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Price](actions/convert-price.md) | `GET /v2/tools/price-conversion` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-market) |
| [Get API Key Info](actions/get-api-key-info.md) | `GET /v1/key/info` | [docs](https://coinmarketcap.com/api/documentation/guides/authentication) |
| [Get Cryptocurrency Categories](actions/get-cryptocurrency-categories.md) | `GET /v1/cryptocurrency/categories` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto) |
| [Get Cryptocurrency Gainers and Losers](actions/get-cryptocurrency-gainers-and-losers.md) | `GET /v1/cryptocurrency/trending/gainers-losers` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto) |
| [Get Cryptocurrency Info](actions/get-cryptocurrency-info.md) | `GET /v2/cryptocurrency/info` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto) |
| [Get Cryptocurrency Map](actions/get-cryptocurrency-map.md) | `GET /v1/cryptocurrency/map` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto) |
| [Get Cryptocurrency Market Pairs](actions/get-cryptocurrency-market-pairs.md) | `GET /v2/cryptocurrency/market-pairs/latest` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto) |
| [Get Cryptocurrency Price Performance Stats](actions/get-cryptocurrency-price-performance-stats.md) | `GET /v2/cryptocurrency/price-performance-stats/latest` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto) |
| [Get Exchange Map](actions/get-exchange-map.md) | `GET /v1/exchange/map` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-exchange) |
| [Get Exchange Market Pairs](actions/get-exchange-market-pairs.md) | `GET /v1/exchange/market-pairs/latest` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-exchange) |
| [Get Historical CMC100 Index](actions/get-historical-cmc100-index.md) | `GET /v3/index/cmc100-historical` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-market) |
| [Get Historical Cryptocurrency OHLCV](actions/get-historical-cryptocurrency-ohlcv.md) | `GET /v2/cryptocurrency/ohlcv/historical` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto) |
| [Get Historical Cryptocurrency Quotes](actions/get-historical-cryptocurrency-quotes.md) | `GET /v3/cryptocurrency/quotes/historical` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto) |
| [Get Historical Fear and Greed Index](actions/get-historical-fear-and-greed-index.md) | `GET /v3/fear-and-greed/historical` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-market) |
| [Get Historical Global Metrics](actions/get-historical-global-metrics.md) | `GET /v1/global-metrics/quotes/historical` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-market) |
| [Get Latest CMC100 Index](actions/get-latest-cmc100-index.md) | `GET /v3/index/cmc100-latest` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-market) |
| [Get Latest Cryptocurrency Listings](actions/get-latest-cryptocurrency-listings.md) | `GET /v3/cryptocurrency/listings/latest` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto) |
| [Get Latest Cryptocurrency OHLCV](actions/get-latest-cryptocurrency-ohlcv.md) | `GET /v2/cryptocurrency/ohlcv/latest` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto) |
| [Get Latest Cryptocurrency Quotes](actions/get-latest-cryptocurrency-quotes.md) | `GET /v3/cryptocurrency/quotes/latest` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto) |
| [Get Latest Exchange Listings](actions/get-latest-exchange-listings.md) | `GET /v1/exchange/listings/latest` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-exchange) |
| [Get Latest Fear and Greed Index](actions/get-latest-fear-and-greed-index.md) | `GET /v3/fear-and-greed/latest` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-market) |
| [Get Latest Global Metrics](actions/get-latest-global-metrics.md) | `GET /v1/global-metrics/quotes/latest` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-market) |
| [Get Latest Trending Cryptocurrencies](actions/get-latest-trending-cryptocurrencies.md) | `GET /v1/cryptocurrency/trending/latest` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto) |
| [Get Most Visited Cryptocurrencies](actions/get-most-visited-cryptocurrencies.md) | `GET /v1/cryptocurrency/trending/most-visited` | [docs](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto) |

# Finnhub: Native API Reference

A consolidated summary of Finnhub's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://finnhub.io/docs/api
- **OpenAPI specification:** https://raw.githubusercontent.com/Finnhub-Stock-API/finnhub-go/master/api/openapi.yaml
- **API base URL:** `https://finnhub.io/api/v1`

## Authentication

### API Key

Connect with a Finnhub API key. Requests send the key as the shared `token` query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://finnhub.io/docs/api)

### Query Token

Connect with a Finnhub API key. Requests send the key only as the shared `token` query parameter.

### Credentials

- **API Key:** `apiKey` · required · Finnhub API key used as the `token` query parameter.

[Official authentication documentation](https://finnhub.io/docs/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Basic Financials](actions/get-basic-financials.md) | `GET /stock/metric` | [docs](https://finnhub.io/docs/api#company-basic-financials) |
| [Get Company Profile](actions/get-company-profile.md) | `GET /stock/profile2` | [docs](https://finnhub.io/docs/api#company-profile2) |
| [Get Forex Rates](actions/get-forex-rates.md) | `GET /forex/rates` | [docs](https://finnhub.io/docs/api#forex-rates) |
| [Get Market News](actions/get-market-news.md) | `GET /news` | [docs](https://finnhub.io/docs/api#market-news) |
| [Get Market Status](actions/get-market-status.md) | `GET /stock/market-status` | [docs](https://finnhub.io/docs/api#market-status) |
| [Get News Sentiment](actions/get-news-sentiment.md) | `GET /news-sentiment` | [docs](https://finnhub.io/docs/api#news-sentiment) |
| [Get Price Target](actions/get-price-target.md) | `GET /stock/price-target` | [docs](https://finnhub.io/docs/api#price-target) |
| [Get Recommendation Trends](actions/get-recommendation-trends.md) | `GET /stock/recommendation` | [docs](https://finnhub.io/docs/api#recommendation-trends) |
| [Get Stock Candles](actions/get-stock-candles.md) | `GET /stock/candle` | [docs](https://finnhub.io/docs/api#stock-candles) |
| [Get Stock Quote](actions/get-stock-quote.md) | `GET /quote` | [docs](https://finnhub.io/docs/api#quote) |
| [List Company News](actions/list-company-news.md) | `GET /company-news` | [docs](https://finnhub.io/docs/api#company-news) |
| [List Company Peers](actions/list-company-peers.md) | `GET /stock/peers` | [docs](https://finnhub.io/docs/api#company-peers) |
| [List Crypto Exchanges](actions/list-crypto-exchanges.md) | `GET /crypto/exchange` | [docs](https://finnhub.io/docs/api#crypto-exchanges) |
| [List Crypto Symbols](actions/list-crypto-symbols.md) | `GET /crypto/symbol` | [docs](https://finnhub.io/docs/api#crypto-symbols) |
| [List Dividends](actions/list-dividends.md) | `GET /stock/dividend` | [docs](https://finnhub.io/docs/api#stock-dividends) |
| [List Earnings Calendar](actions/list-earnings-calendar.md) | `GET /calendar/earnings` | [docs](https://finnhub.io/docs/api#earnings-calendar) |
| [List Earnings Surprises](actions/list-earnings-surprises.md) | `GET /stock/earnings` | [docs](https://finnhub.io/docs/api#company-earnings) |
| [List Forex Exchanges](actions/list-forex-exchanges.md) | `GET /forex/exchange` | [docs](https://finnhub.io/docs/api#forex-exchanges) |
| [List Forex Symbols](actions/list-forex-symbols.md) | `GET /forex/symbol` | [docs](https://finnhub.io/docs/api#forex-symbols) |
| [List IPO Calendar](actions/list-ipo-calendar.md) | `GET /calendar/ipo` | [docs](https://finnhub.io/docs/api#ipo-calendar) |
| [List Market Holidays](actions/list-market-holidays.md) | `GET /stock/market-holiday` | [docs](https://finnhub.io/docs/api#market-holiday) |
| [List Stock Symbols](actions/list-stock-symbols.md) | `GET /stock/symbol` | [docs](https://finnhub.io/docs/api#stock-symbols) |
| [List Stock Upgrades Downgrades](actions/list-stock-upgrades-downgrades.md) | `GET /stock/upgrade-downgrade` | [docs](https://finnhub.io/docs/api#upgrade-downgrade) |
| [Search Symbols](actions/search-symbols.md) | `GET /search` | [docs](https://finnhub.io/docs/api#symbol-search) |

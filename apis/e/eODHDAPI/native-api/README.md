# EODHD: Native API Reference

A consolidated summary of EODHD's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://eodhd.com/financial-apis/quick-start-with-our-financial-data-apis/
- **API base URL:** `https://eodhd.com/api`

## Authentication

### API Key

Connect with an EODHD API token. Requests send the stored key as the shared `api_token` query parameter. Copy the token from the EODHD user dashboard and keep it private because EODHD uses it for plan access and API call quota.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://eodhd.com/financial-apis/quick-start-with-our-financial-data-apis/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Analyst Ratings](actions/get-analyst-ratings.md) | `GET /fundamentals/{symbol}` | [docs](https://eodhd.com/financial-apis/stock-etfs-fundamental-data-feeds/) |
| [Get Balance Sheet Fundamentals](actions/get-balance-sheet-fundamentals.md) | `GET /fundamentals/{symbol}` | [docs](https://eodhd.com/financial-apis/stock-etfs-fundamental-data-feeds/) |
| [Get Cash Flow Fundamentals](actions/get-cash-flow-fundamentals.md) | `GET /fundamentals/{symbol}` | [docs](https://eodhd.com/financial-apis/stock-etfs-fundamental-data-feeds/) |
| [Get Earnings Fundamentals](actions/get-earnings-fundamentals.md) | `GET /fundamentals/{symbol}` | [docs](https://eodhd.com/financial-apis/stock-etfs-fundamental-data-feeds/) |
| [Get Exchange Details](actions/get-exchange-details.md) | `GET /exchange-details/{exchangeCode}` | [docs](https://eodhd.com/financial-apis/exchanges-api-trading-hours-and-stock-market-holidays/) |
| [Get Full Fundamentals](actions/get-full-fundamentals.md) | `GET /fundamentals/{symbol}` | [docs](https://eodhd.com/financial-apis/stock-etfs-fundamental-data-feeds/) |
| [Get Fundamental Highlights](actions/get-fundamental-highlights.md) | `GET /fundamentals/{symbol}` | [docs](https://eodhd.com/financial-apis/stock-etfs-fundamental-data-feeds/) |
| [Get General Fundamentals](actions/get-general-fundamentals.md) | `GET /fundamentals/{symbol}` | [docs](https://eodhd.com/financial-apis/stock-etfs-fundamental-data-feeds/) |
| [Get Historical Index Constituents](actions/get-historical-index-constituents.md) | `GET /fundamentals/{indexSymbol}` | [docs](https://eodhd.com/financial-apis/stock-etfs-fundamental-data-feeds/) |
| [Get Historical Market Cap](actions/get-historical-market-cap.md) | `GET /historical-market-cap/{symbol}` | [docs](https://eodhd.com/financial-apis/historical-market-capitalization-api/) |
| [Get Holders](actions/get-holders.md) | `GET /fundamentals/{symbol}` | [docs](https://eodhd.com/financial-apis/stock-etfs-fundamental-data-feeds/) |
| [Get Income Statement Fundamentals](actions/get-income-statement-fundamentals.md) | `GET /fundamentals/{symbol}` | [docs](https://eodhd.com/financial-apis/stock-etfs-fundamental-data-feeds/) |
| [Get Latest EOD Close](actions/get-latest-eod-close.md) | `GET /eod/{symbol}` | [docs](https://eodhd.com/financial-apis/api-for-historical-data-and-volumes/) |
| [Get Macro Indicator](actions/get-macro-indicator.md) | `GET /macro-indicator/{country}` | [docs](https://eodhd.com/financial-apis/macroeconomics-data-and-macro-indicators-api/) |
| [Get News Sentiment](actions/get-news-sentiment.md) | `GET /sentiments` | [docs](https://eodhd.com/financial-apis/stock-market-financial-news-api/) |
| [Get News Word Weights](actions/get-news-word-weights.md) | `GET /news-word-weights` | [docs](https://eodhd.com/financial-apis/stock-market-financial-news-api/) |
| [Get Real-Time Quote](actions/get-real-time-quote.md) | `GET /real-time/{symbol}` | [docs](https://eodhd.com/financial-apis/live-ohlcv-stocks-api/) |
| [Get Share Statistics](actions/get-share-statistics.md) | `GET /fundamentals/{symbol}` | [docs](https://eodhd.com/financial-apis/stock-etfs-fundamental-data-feeds/) |
| [Get Technical Indicator](actions/get-technical-indicator.md) | `GET /technical/{symbol}` | [docs](https://eodhd.com/financial-apis/technical-indicators-api/) |
| [Get Valuation Metrics](actions/get-valuation-metrics.md) | `GET /fundamentals/{symbol}` | [docs](https://eodhd.com/financial-apis/stock-etfs-fundamental-data-feeds/) |
| [List Delisted Exchange Symbols](actions/list-delisted-exchange-symbols.md) | `GET /exchange-symbol-list/{exchangeCode}` | [docs](https://eodhd.com/financial-apis/exchanges-api-list-of-tickers-and-trading-hours/) |
| [List Dividends Calendar](actions/list-dividends-calendar.md) | `GET /calendar/dividends` | [docs](https://eodhd.com/financial-apis/calendar-upcoming-earnings-ipos-and-splits/) |
| [List Earnings Calendar](actions/list-earnings-calendar.md) | `GET /calendar/earnings` | [docs](https://eodhd.com/financial-apis/calendar-upcoming-earnings-ipos-and-splits/) |
| [List Earnings Trends](actions/list-earnings-trends.md) | `GET /calendar/trends` | [docs](https://eodhd.com/financial-apis/calendar-upcoming-earnings-ipos-and-splits/) |
| [List Economic Events](actions/list-economic-events.md) | `GET /economic-events` | [docs](https://eodhd.com/financial-apis/economic-events-data-api/) |
| [List EOD Historical Prices](actions/list-eod-historical-prices.md) | `GET /eod/{symbol}` | [docs](https://eodhd.com/financial-apis/api-for-historical-data-and-volumes/) |
| [List Exchange Symbols](actions/list-exchange-symbols.md) | `GET /exchange-symbol-list/{exchangeCode}` | [docs](https://eodhd.com/financial-apis/exchanges-api-list-of-tickers-and-trading-hours/) |
| [List Financial News](actions/list-financial-news.md) | `GET /news` | [docs](https://eodhd.com/financial-apis/stock-market-financial-news-api/) |
| [List Historical Dividends](actions/list-historical-dividends.md) | `GET /div/{symbol}` | [docs](https://eodhd.com/financial-apis/api-splits-dividends/) |
| [List Historical Splits](actions/list-historical-splits.md) | `GET /splits/{symbol}` | [docs](https://eodhd.com/financial-apis/api-splits-dividends/) |
| [List Intraday Prices](actions/list-intraday-prices.md) | `GET /intraday/{symbol}` | [docs](https://eodhd.com/financial-apis/intraday-historical-data-api/) |
| [List IPO Calendar](actions/list-ipo-calendar.md) | `GET /calendar/ipos` | [docs](https://eodhd.com/financial-apis/calendar-upcoming-earnings-ipos-and-splits/) |
| [List Splits Calendar](actions/list-splits-calendar.md) | `GET /calendar/splits` | [docs](https://eodhd.com/financial-apis/calendar-upcoming-earnings-ipos-and-splits/) |
| [List Supported Crypto Symbols](actions/list-supported-crypto-symbols.md) | `GET /exchange-symbol-list/{exchangeCode}` | [docs](https://eodhd.com/financial-apis/list-supported-crypto-currencies/) |
| [List Supported Exchanges](actions/list-supported-exchanges.md) | `GET /exchanges-list/` | [docs](https://eodhd.com/financial-apis/exchanges-api-list-of-tickers-and-trading-hours/) |
| [List Supported Forex Pairs](actions/list-supported-forex-pairs.md) | `GET /exchange-symbol-list/{exchangeCode}` | [docs](https://eodhd.com/financial-apis/list-supported-forex-currencies/) |
| [List Symbol Change History](actions/list-symbol-change-history.md) | `GET /symbol-change-history` | [docs](https://eodhd.com/financial-apis/exchanges-api-trading-hours-and-stock-market-holidays/) |
| [List US Real-Time Quotes](actions/list-us-real-time-quotes.md) | `GET /real-time/{symbol}` | [docs](https://eodhd.com/financial-apis/bulk-for-live-ohlcv-stock-prices-api-us-exchanges-only/) |
| [Screen Stocks](actions/screen-stocks.md) | `GET /screener` | [docs](https://eodhd.com/financial-apis/stock-market-screener-api/) |
| [Search Instruments](actions/search-instruments.md) | `GET /search/{query}` | [docs](https://eodhd.com/financial-apis/search-api-for-stocks-etfs-mutual-funds-and-indices/) |

# <img src="https://images.mindcloud.co/apps/icons/e-odhdapi_1776261536114.png" alt="EODHD logo" width="28" height="28"> EODHD: Universal API

Financial market data APIs for EOD prices, live quotes, fundamentals, corporate actions, calendars, news, screeners, technical indicators, macro indicators, and exchange reference data from EODHD.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eODHDAPI/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://eodhd.com
- **Vendor API docs:** https://eodhd.com/financial-apis/quick-start-with-our-financial-data-apis/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Supported Exchanges](actions/list-supported-exchanges.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-supported-exchanges?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Analyst Ratings

| Action | Method | Description |
| --- | --- | --- |
| [Get Analyst Ratings](actions/get-analyst-ratings.md) | GET | Retrieves analyst ratings for a symbol from EODHD API. |

### Balance Sheet Fundamentals

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance Sheet Fundamentals](actions/get-balance-sheet-fundamentals.md) | GET | Retrieves balance sheet fundamentals for a symbol from EODHD API. |

### Cash Flow Fundamentals

| Action | Method | Description |
| --- | --- | --- |
| [Get Cash Flow Fundamentals](actions/get-cash-flow-fundamentals.md) | GET | Retrieves cash flow fundamentals for a symbol from EODHD API. |

### Crypto Symbol

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Crypto Symbols](actions/list-supported-crypto-symbols.md) | GET | Retrieves supported cryptocurrency symbols from EODHD API. |

### Delisted Exchange Symbol

| Action | Method | Description |
| --- | --- | --- |
| [List Delisted Exchange Symbols](actions/list-delisted-exchange-symbols.md) | GET | Retrieves delisted symbols for an exchange from EODHD API. |

### Dividend

| Action | Method | Description |
| --- | --- | --- |
| [List Historical Dividends](actions/list-historical-dividends.md) | GET | Retrieves historical dividends for a symbol from EODHD API. |

### Dividends Calendar

| Action | Method | Description |
| --- | --- | --- |
| [List Dividends Calendar](actions/list-dividends-calendar.md) | GET | Retrieves dividend calendar events from EODHD API. |

### Earnings Calendar

| Action | Method | Description |
| --- | --- | --- |
| [List Earnings Calendar](actions/list-earnings-calendar.md) | GET | Retrieves earnings calendar events from EODHD API. |

### Earnings Fundamentals

| Action | Method | Description |
| --- | --- | --- |
| [Get Earnings Fundamentals](actions/get-earnings-fundamentals.md) | GET | Retrieves earnings fundamentals for a symbol from EODHD API. |

### Earnings Trend

| Action | Method | Description |
| --- | --- | --- |
| [List Earnings Trends](actions/list-earnings-trends.md) | GET | Retrieves earnings trends for symbols from EODHD API. |

### Economic Event

| Action | Method | Description |
| --- | --- | --- |
| [List Economic Events](actions/list-economic-events.md) | GET | Retrieves economic events from EODHD API. |

### Eod Historical Price

| Action | Method | Description |
| --- | --- | --- |
| [List EOD Historical Prices](actions/list-eod-historical-prices.md) | GET | Retrieves end-of-day historical prices for a symbol from EODHD API. |

### Exchange

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Exchanges](actions/list-supported-exchanges.md) | GET | Retrieves supported exchanges from EODHD API. |

### Exchange Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Exchange Details](actions/get-exchange-details.md) | GET | Retrieves trading hours and holidays for an exchange from EODHD API. |

### Exchange Symbol

| Action | Method | Description |
| --- | --- | --- |
| [List Exchange Symbols](actions/list-exchange-symbols.md) | GET | Retrieves symbols for an exchange from EODHD API. |

### Financial News

| Action | Method | Description |
| --- | --- | --- |
| [List Financial News](actions/list-financial-news.md) | GET | Retrieves financial news for symbols or tags from EODHD API. |

### Forex Pair

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Forex Pairs](actions/list-supported-forex-pairs.md) | GET | Retrieves supported forex pairs from EODHD API. |

### Fundamental Highlights

| Action | Method | Description |
| --- | --- | --- |
| [Get Fundamental Highlights](actions/get-fundamental-highlights.md) | GET | Retrieves fundamental highlights for a symbol from EODHD API. |

### Fundamentals

| Action | Method | Description |
| --- | --- | --- |
| [Get Full Fundamentals](actions/get-full-fundamentals.md) | GET | Retrieves full fundamentals for a symbol from EODHD API. |

### General Fundamentals

| Action | Method | Description |
| --- | --- | --- |
| [Get General Fundamentals](actions/get-general-fundamentals.md) | GET | Retrieves general fundamentals for a symbol from EODHD API. |

### Historical Index Constituent

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Index Constituents](actions/get-historical-index-constituents.md) | GET | Retrieves historical index constituents from EODHD API. |

### Historical Market Cap

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Market Cap](actions/get-historical-market-cap.md) | GET | Retrieves historical market capitalization for a symbol from EODHD API. |

### Holders

| Action | Method | Description |
| --- | --- | --- |
| [Get Holders](actions/get-holders.md) | GET | Retrieves holder data for a symbol from EODHD API. |

### Income Statement Fundamentals

| Action | Method | Description |
| --- | --- | --- |
| [Get Income Statement Fundamentals](actions/get-income-statement-fundamentals.md) | GET | Retrieves income statement fundamentals for a symbol from EODHD API. |

### Instrument Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Instruments](actions/search-instruments.md) | GET | Finds instruments in EODHD API by keyword. |

### Intraday Price

| Action | Method | Description |
| --- | --- | --- |
| [List Intraday Prices](actions/list-intraday-prices.md) | GET | Retrieves intraday prices for a symbol from EODHD API. |

### Ipo Calendar

| Action | Method | Description |
| --- | --- | --- |
| [List IPO Calendar](actions/list-ipo-calendar.md) | GET | Retrieves IPO calendar events from EODHD API. |

### Latest Eod Close

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest EOD Close](actions/get-latest-eod-close.md) | GET | Retrieves the latest end-of-day close for a symbol from EODHD API. |

### Macro Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get Macro Indicator](actions/get-macro-indicator.md) | GET | Retrieves a macroeconomic indicator by country from EODHD API. |

### News Sentiment

| Action | Method | Description |
| --- | --- | --- |
| [Get News Sentiment](actions/get-news-sentiment.md) | GET | Retrieves news sentiment for a symbol from EODHD API. |

### News Word Weights

| Action | Method | Description |
| --- | --- | --- |
| [Get News Word Weights](actions/get-news-word-weights.md) | GET | Retrieves news word weights for a symbol from EODHD API. |

### Real-time Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Real-Time Quote](actions/get-real-time-quote.md) | GET | Retrieves a real-time quote for a symbol from EODHD API. |

### Share Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Share Statistics](actions/get-share-statistics.md) | GET | Retrieves share statistics for a symbol from EODHD API. |

### Split

| Action | Method | Description |
| --- | --- | --- |
| [List Historical Splits](actions/list-historical-splits.md) | GET | Retrieves historical splits for a symbol from EODHD API. |

### Splits Calendar

| Action | Method | Description |
| --- | --- | --- |
| [List Splits Calendar](actions/list-splits-calendar.md) | GET | Retrieves stock split calendar events from EODHD API. |

### Stock Screener Result

| Action | Method | Description |
| --- | --- | --- |
| [Screen Stocks](actions/screen-stocks.md) | GET | Finds stocks in EODHD API using screener filters. |

### Symbol Change

| Action | Method | Description |
| --- | --- | --- |
| [List Symbol Change History](actions/list-symbol-change-history.md) | GET | Retrieves stock symbol change history from EODHD API. |

### Technical Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get Technical Indicator](actions/get-technical-indicator.md) | GET | Retrieves a technical indicator for a symbol from EODHD API. |

### Us Real-time Quote

| Action | Method | Description |
| --- | --- | --- |
| [List US Real-Time Quotes](actions/list-us-real-time-quotes.md) | GET | Retrieves real-time quotes for US symbols from EODHD API. |

### Valuation Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Valuation Metrics](actions/get-valuation-metrics.md) | GET | Retrieves valuation metrics for a symbol from EODHD API. |


# <img src="https://images.mindcloud.co/apps/icons/finnhub_1776201386738.png" alt="Finnhub logo" width="28" height="28"> Finnhub: Universal API

Access stock, forex, crypto, company fundamentals, news, calendars, and market data from Finnhub.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/finnhub/latest
- **Category:** Commerce / Accounting
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://finnhub.io
- **Vendor API docs:** https://finnhub.io/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Stock Quote](actions/get-stock-quote.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-stock-quote?connectionId=$CONNECTION_ID&symbol=e.g.%20AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Basic Financial

| Action | Method | Description |
| --- | --- | --- |
| [Get Basic Financials](actions/get-basic-financials.md) | GET | Retrieves basic financials from Finnhub. |

### Company News

| Action | Method | Description |
| --- | --- | --- |
| [List Company News](actions/list-company-news.md) | GET | Retrieves company news from Finnhub. |

### Company Peer

| Action | Method | Description |
| --- | --- | --- |
| [List Company Peers](actions/list-company-peers.md) | GET | Retrieves company peers from Finnhub. |

### Company Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Profile](actions/get-company-profile.md) | GET | Retrieves a company profile from Finnhub. |

### Crypto Exchange

| Action | Method | Description |
| --- | --- | --- |
| [List Crypto Exchanges](actions/list-crypto-exchanges.md) | GET | Retrieves crypto exchanges from Finnhub. |

### Crypto Symbol

| Action | Method | Description |
| --- | --- | --- |
| [List Crypto Symbols](actions/list-crypto-symbols.md) | GET | Retrieves crypto symbols from Finnhub. |

### Dividend

| Action | Method | Description |
| --- | --- | --- |
| [List Dividends](actions/list-dividends.md) | GET | Retrieves dividends from Finnhub. |

### Earnings Calendar

| Action | Method | Description |
| --- | --- | --- |
| [List Earnings Calendar](actions/list-earnings-calendar.md) | GET | Retrieves the earnings calendar from Finnhub. |

### Earnings Surprise

| Action | Method | Description |
| --- | --- | --- |
| [List Earnings Surprises](actions/list-earnings-surprises.md) | GET | Retrieves earnings surprises from Finnhub. |

### Forex Exchange

| Action | Method | Description |
| --- | --- | --- |
| [List Forex Exchanges](actions/list-forex-exchanges.md) | GET | Retrieves forex exchanges from Finnhub. |

### Forex Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Forex Rates](actions/get-forex-rates.md) | GET | Retrieves forex rates from Finnhub. |

### Forex Symbol

| Action | Method | Description |
| --- | --- | --- |
| [List Forex Symbols](actions/list-forex-symbols.md) | GET | Retrieves forex symbols from Finnhub. |

### Ipo Calendar

| Action | Method | Description |
| --- | --- | --- |
| [List IPO Calendar](actions/list-ipo-calendar.md) | GET | Retrieves the IPO calendar from Finnhub. |

### Market Holiday

| Action | Method | Description |
| --- | --- | --- |
| [List Market Holidays](actions/list-market-holidays.md) | GET | Retrieves market holidays from Finnhub. |

### Market News

| Action | Method | Description |
| --- | --- | --- |
| [Get Market News](actions/get-market-news.md) | GET | Retrieves market news from Finnhub. |

### Market Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Market Status](actions/get-market-status.md) | GET | Retrieves market status from Finnhub. |

### News Sentiment

| Action | Method | Description |
| --- | --- | --- |
| [Get News Sentiment](actions/get-news-sentiment.md) | GET | Retrieves news sentiment from Finnhub. |

### Price Target

| Action | Method | Description |
| --- | --- | --- |
| [Get Price Target](actions/get-price-target.md) | GET | Retrieves a price target from Finnhub. |

### Recommendation Trend

| Action | Method | Description |
| --- | --- | --- |
| [Get Recommendation Trends](actions/get-recommendation-trends.md) | GET | Retrieves recommendation trends from Finnhub. |

### Stock Candle

| Action | Method | Description |
| --- | --- | --- |
| [Get Stock Candles](actions/get-stock-candles.md) | GET | Retrieves stock candles from Finnhub. |

### Stock Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Stock Quote](actions/get-stock-quote.md) | GET | Retrieves a stock quote from Finnhub. |

### Stock Symbol

| Action | Method | Description |
| --- | --- | --- |
| [List Stock Symbols](actions/list-stock-symbols.md) | GET | Retrieves stock symbols from Finnhub. |

### Stock Upgrade Downgrade

| Action | Method | Description |
| --- | --- | --- |
| [List Stock Upgrades Downgrades](actions/list-stock-upgrades-downgrades.md) | GET | Retrieves stock upgrades and downgrades from Finnhub. |

### Symbol

| Action | Method | Description |
| --- | --- | --- |
| [Search Symbols](actions/search-symbols.md) | GET | Finds symbols in Finnhub by search text. |


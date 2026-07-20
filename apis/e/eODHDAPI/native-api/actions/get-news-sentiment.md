# Get News Sentiment with EODHD

Retrieves news sentiment for a symbol from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/sentiments`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [Get News Sentiment](https://eodhd.com/financial-apis/stock-market-financial-news-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `s` | query | `string` | yes | Ticker symbol, for example aapl.us. |
| `from` | query | `date` | no | Start date in YYYY-MM-DD format. |
| `to` | query | `date` | no | End date in YYYY-MM-DD format. |

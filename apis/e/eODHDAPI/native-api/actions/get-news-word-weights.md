# Get News Word Weights with EODHD

Retrieves news word weights for a symbol from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/news-word-weights`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [Get News Word Weights](https://eodhd.com/financial-apis/stock-market-financial-news-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `s` | query | `string` | yes | Ticker symbol, for example AAPL. |
| `filter[date_from]` | query | `date` | no | Start date for the word-weights date filter in YYYY-MM-DD format. |
| `filter[to]` | query | `date` | no | End date for the word-weights date filter in YYYY-MM-DD format. |
| `page[limit]` | query | `number` | no | Maximum number of word-weight rows to return. |

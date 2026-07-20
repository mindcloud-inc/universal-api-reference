# List Financial News with EODHD

Retrieves financial news for symbols or tags from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/news`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [List Financial News](https://eodhd.com/financial-apis/stock-market-financial-news-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `s` | query | `string` | no | Comma-separated symbols, for example AAPL.US. |
| `offset` | query | `number` | no | Number of news items to skip. |
| `limit` | query | `number` | no | Maximum number of news items to return. |

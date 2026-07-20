# Screen Stocks with EODHD

Finds stocks in EODHD API using screener filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/screener`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [Screen Stocks](https://eodhd.com/financial-apis/stock-market-screener-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | query | `string` | no | JSON filter expression array for the screener endpoint. |
| `signals` | query | `string` | no | Comma-separated predefined screener signals. |
| `sort` | query | `string` | no | Sort field and direction, for example market_capitalization.desc. |
| `limit` | query | `number` | no | Maximum number of screener results to return. |
| `offset` | query | `number` | no | Number of screener results to skip. |

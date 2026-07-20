# List Dividends with Finnhub

Retrieves dividends from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/stock/dividend`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [List Dividends](https://finnhub.io/docs/api#stock-dividends)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | query | `string` | yes | Company symbol, such as AAPL. |
| `from` | query | `string` | yes | Start date in YYYY-MM-DD format. |
| `to` | query | `string` | yes | End date in YYYY-MM-DD format. |

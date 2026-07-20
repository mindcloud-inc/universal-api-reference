# List Company News with Finnhub

Retrieves company news from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/company-news`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [List Company News](https://finnhub.io/docs/api#company-news)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | query | `string` | yes | Company symbol for news, such as AAPL. |
| `from` | query | `string` | yes | Start date in YYYY-MM-DD format. |
| `to` | query | `string` | yes | End date in YYYY-MM-DD format. |

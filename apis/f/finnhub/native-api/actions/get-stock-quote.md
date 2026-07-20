# Get Stock Quote with Finnhub

Retrieves a stock quote from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/quote`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [Get Stock Quote](https://finnhub.io/docs/api#quote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | query | `string` | yes | Company symbol for the quote, such as AAPL. |

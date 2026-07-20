# Get Stock Candles with Finnhub

Retrieves stock candles from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/stock/candle`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [Get Stock Candles](https://finnhub.io/docs/api#stock-candles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | query | `string` | yes | Company symbol for candles, such as AAPL. |
| `resolution` | query | `string` | yes | Supported candle resolution, such as 1, 5, 15, 30, 60, D, W, or M. |
| `from` | query | `number` | yes | Start time as a UNIX timestamp in seconds. |
| `to` | query | `number` | yes | End time as a UNIX timestamp in seconds. |

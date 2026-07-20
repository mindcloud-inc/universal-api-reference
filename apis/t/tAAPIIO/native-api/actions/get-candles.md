# Get Candles with TAAPI.IO

Retrieves candlestick data for a market from TAAPI.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/candles`
- **Base URL:** `https://api.taapi.io`
- **Official documentation:** [Get Candles](https://taapi.io/indicators/candles/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `exchange` | query | `string` | yes |
| `symbol` | query | `string` | yes |
| `interval` | query | `string` | yes |

# Get Average Directional Movement Index Rating with TAAPI.IO

Retrieves Average Directional Movement Index Rating data from TAAPI.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/adxr`
- **Base URL:** `https://api.taapi.io`
- **Official documentation:** [Get Average Directional Movement Index Rating](https://taapi.io/indicators/average-directional-movement-index-rating/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exchange` | query | `string` | yes | Exchange to source the indicator data from, such as binance. |
| `symbol` | query | `string` | yes | Trading pair symbol such as BTC/USDT. |
| `interval` | query | `string` | yes | Timeframe such as 1h or 1d. |
| `period` | query | `number` | no | Optional candle count used in the indicator calculation. |

# Get Williams %R with TAAPI.IO

Retrieves Williams %R indicator data from TAAPI.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/willr`
- **Base URL:** `https://api.taapi.io`
- **Official documentation:** [Get Williams %R](https://taapi.io/indicators/williams-r/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exchange` | query | `string` | yes | Exchange to source the indicator data from, such as binance. |
| `symbol` | query | `string` | yes | Trading pair symbol such as BTC/USDT. |
| `interval` | query | `string` | yes | Timeframe such as 1h or 1d. |
| `period` | query | `number` | no | Optional candle count used in the indicator calculation. |

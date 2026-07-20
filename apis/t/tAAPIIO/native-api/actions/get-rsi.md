# Get RSI with TAAPI.IO

Retrieves RSI indicator data from TAAPI.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/rsi`
- **Base URL:** `https://api.taapi.io`
- **Official documentation:** [Get RSI](https://taapi.io/indicators/relative-strength-index-rsi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exchange` | query | `string` | yes | Exchange to source the indicator data from, such as binance. |
| `symbol` | query | `string` | yes | Trading pair symbol such as BTC/USDT. |
| `interval` | query | `string` | yes | Timeframe such as 1h or 1d. |
| `period` | query | `number` | no | — |
| `backtrack` | query | `number` | no | — |
| `chart` | query | `string` | no | — |
| `addResultTimestamp` | query | `boolean` | no | — |
| `fromTimestamp` | query | `string` | no | — |
| `toTimestamp` | query | `string` | no | — |
| `results` | query | `string` | no | — |

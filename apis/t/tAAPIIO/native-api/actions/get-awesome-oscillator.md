# Get Awesome Oscillator with TAAPI.IO

Retrieves Awesome Oscillator indicator data from TAAPI.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/ao`
- **Base URL:** `https://api.taapi.io`
- **Official documentation:** [Get Awesome Oscillator](https://taapi.io/indicators/awesome-oscillator/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exchange` | query | `string` | yes | Exchange to source the indicator data from, such as binance. |
| `symbol` | query | `string` | yes | Trading pair symbol such as BTC/USDT. |
| `interval` | query | `string` | yes | Timeframe such as 1h or 1d. |

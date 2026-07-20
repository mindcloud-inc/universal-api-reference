# Get Accelerator Oscillator with TAAPI.IO

Retrieves Accelerator Oscillator indicator data from TAAPI.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/accosc`
- **Base URL:** `https://api.taapi.io`
- **Official documentation:** [Get Accelerator Oscillator](https://taapi.io/indicators/accelerator-oscillator/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exchange` | query | `string` | yes | Exchange to source the indicator data from, such as binance. |
| `symbol` | query | `string` | yes | Trading pair symbol such as BTC/USDT. |
| `interval` | query | `string` | yes | Timeframe such as 1h or 1d. |
| `lengthSlow` | query | `number` | no | Optional slow length for the oscillator calculation. |
| `lengthFast` | query | `number` | no | Optional fast length for the oscillator calculation. |

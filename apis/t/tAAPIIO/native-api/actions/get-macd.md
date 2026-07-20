# Get MACD with TAAPI.IO

Retrieves MACD indicator data from TAAPI.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/macd`
- **Base URL:** `https://api.taapi.io`
- **Official documentation:** [Get MACD](https://taapi.io/indicators/macd/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `exchange` | query | `string` | yes |
| `symbol` | query | `string` | yes |
| `interval` | query | `string` | yes |

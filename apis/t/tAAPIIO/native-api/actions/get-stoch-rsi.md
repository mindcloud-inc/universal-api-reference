# Get StochRSI with TAAPI.IO

Retrieves StochRSI indicator data from TAAPI.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/stochrsi`
- **Base URL:** `https://api.taapi.io`
- **Official documentation:** [Get StochRSI](https://taapi.io/indicators/stochrsi-stochastic-relative-strength-index/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `exchange` | query | `string` | yes |
| `symbol` | query | `string` | yes |
| `interval` | query | `string` | yes |

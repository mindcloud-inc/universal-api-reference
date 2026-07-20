# Get VWAP with TAAPI.IO

Retrieves VWAP indicator data from TAAPI.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/vwap`
- **Base URL:** `https://api.taapi.io`
- **Official documentation:** [Get VWAP](https://taapi.io/indicators/volume-weighted-average-price-vwap/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `exchange` | query | `string` | yes |
| `symbol` | query | `string` | yes |
| `interval` | query | `string` | yes |

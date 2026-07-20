# Get Forex Daily with Alpha Vantage

Retrieves forex daily data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get Forex Daily](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_symbol` | query | `string` | yes | Query parameter $key for FX_DAILY. |
| `outputsize` | query | `string` | no | Query parameter $key for FX_DAILY. |
| `to_symbol` | query | `string` | yes | Query parameter $key for FX_DAILY. |
| `from_symbol` | query | `string` | yes | Base currency symbol. |
| `to_symbol` | query | `string` | yes | Quote currency symbol. |

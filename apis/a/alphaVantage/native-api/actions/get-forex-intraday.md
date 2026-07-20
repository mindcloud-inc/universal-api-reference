# Get Forex Intraday with Alpha Vantage

Retrieves forex intraday data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get Forex Intraday](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_symbol` | query | `string` | yes | Query parameter $key for FX_INTRADAY. |
| `outputsize` | query | `string` | no | Query parameter $key for FX_INTRADAY. |
| `to_symbol` | query | `string` | yes | Query parameter $key for FX_INTRADAY. |
| `from_symbol` | query | `string` | yes | Base currency symbol. |
| `to_symbol` | query | `string` | yes | Quote currency symbol. |
| `interval` | query | `string` | yes | Query parameter $key for FX_INTRADAY. Accepted values: `0`, `1`, `2`, `3`, `4`. |

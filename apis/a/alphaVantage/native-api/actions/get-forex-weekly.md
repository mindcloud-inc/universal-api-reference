# Get Forex Weekly with Alpha Vantage

Retrieves forex weekly data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get Forex Weekly](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_symbol` | query | `string` | yes | Query parameter $key for FX_WEEKLY. |
| `to_symbol` | query | `string` | yes | Query parameter $key for FX_WEEKLY. |
| `from_symbol` | query | `string` | yes | Base currency symbol. |
| `to_symbol` | query | `string` | yes | Quote currency symbol. |

# Get Forex Monthly with Alpha Vantage

Retrieves forex monthly data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get Forex Monthly](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_symbol` | query | `string` | yes | Query parameter $key for FX_MONTHLY. |
| `to_symbol` | query | `string` | yes | Query parameter $key for FX_MONTHLY. |
| `from_symbol` | query | `string` | yes | Base currency symbol. |
| `to_symbol` | query | `string` | yes | Quote currency symbol. |

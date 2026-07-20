# Get Forex Exchange Rate with Alpha Vantage

Retrieves forex exchange rate data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get Forex Exchange Rate](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_currency` | query | `string` | no | Base currency code. |
| `from_currency` | query | `string` | yes | Query parameter $key for CURRENCY_EXCHANGE_RATE. |
| `to_currency` | query | `string` | no | Quote currency code. |
| `to_currency` | query | `string` | yes | Query parameter $key for CURRENCY_EXCHANGE_RATE. |

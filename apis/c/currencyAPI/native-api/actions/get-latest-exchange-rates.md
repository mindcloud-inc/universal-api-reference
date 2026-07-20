# Get Latest Exchange Rates with CurrencyAPI

Retrieves latest exchange rates from CurrencyAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/latest`
- **Base URL:** `https://api.currencyapi.com`
- **Official documentation:** [Get Latest Exchange Rates](https://currencyapi.com/docs/latest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base_currency` | query | `string` | no | Base currency for the exchange rates. |
| `currencies` | query | `string` | no | Comma-separated currency codes to return. |
| `type` | query | `string` | no | Currency type to return: fiat, metal, or crypto. |

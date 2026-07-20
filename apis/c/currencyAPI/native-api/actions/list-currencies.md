# List Currencies with CurrencyAPI

Retrieves supported currency definitions from CurrencyAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/currencies`
- **Base URL:** `https://api.currencyapi.com`
- **Official documentation:** [List Currencies](https://currencyapi.com/docs/currencies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currencies` | query | `string` | no | Comma-separated currency codes to return. |
| `type` | query | `string` | no | Currency type to return: fiat, metal, or crypto. |

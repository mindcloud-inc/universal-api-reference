# Get Historical Exchange Rates with CurrencyAPI

Retrieves historical exchange rates from CurrencyAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/historical`
- **Base URL:** `https://api.currencyapi.com`
- **Official documentation:** [Get Historical Exchange Rates](https://currencyapi.com/docs/historical)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | yes | Historical date in YYYY-MM-DD format. |
| `base_currency` | query | `string` | no | Base currency for the exchange rates. |
| `currencies` | query | `string` | no | Comma-separated currency codes to return. |
| `type` | query | `string` | no | Currency type to return: fiat, metal, or crypto. |

# Get Exchange Rate with Cloudmersive Currency

Retrieves an exchange rate from Cloudmersive Currency.

## Endpoint

- **Method:** `POST`
- **Path:** `/currency/exchange-rates/get/:source/to/:destination`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Get Exchange Rate](https://api.cloudmersive.com/docs/currency.asp#operation--currency-exchange-rates-get-source-to-destination-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | path | `string` | yes | Source currency three-digit ISO 4217 code, such as USD or EUR. |
| `destination` | path | `string` | yes | Destination currency three-digit ISO 4217 code, such as USD or EUR. |

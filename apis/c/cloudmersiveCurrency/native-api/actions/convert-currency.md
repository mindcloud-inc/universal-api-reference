# Convert Currency with Cloudmersive Currency

Converts a currency amount in Cloudmersive Currency.

## Endpoint

- **Method:** `POST`
- **Path:** `/currency/exchange-rates/convert/:source/to/:destination`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Convert Currency](https://api.cloudmersive.com/docs/currency.asp#operation--currency-exchange-rates-convert-source-to-destination-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | path | `string` | yes | Source currency three-digit ISO 4217 code, such as USD or EUR. |
| `destination` | path | `string` | yes | Destination currency three-digit ISO 4217 code, such as USD or EUR. |
| `price` | body | `number` | yes | Input price in the source currency, such as 19.99. |

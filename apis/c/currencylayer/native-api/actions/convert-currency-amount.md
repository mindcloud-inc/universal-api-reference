# Convert Currency Amount with Currencylayer

Converts a currency amount using Currencylayer rates.

## Endpoint

- **Method:** `GET`
- **Path:** `/convert`
- **Base URL:** `https://api.currencylayer.com`
- **Official documentation:** [Convert Currency Amount](https://currencylayer.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | yes | 3-letter currency code to convert from. |
| `to` | query | `string` | yes | 3-letter currency code to convert to. |
| `amount` | query | `number` | yes | Amount to convert. |

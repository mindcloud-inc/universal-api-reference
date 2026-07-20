# Convert Currency with Exchange Rates API

Converts an amount between currencies in Exchange Rates API.

## Endpoint

- **Method:** `GET`
- **Path:** `convert`
- **Base URL:** `https://api.exchangeratesapi.io/v1`
- **Official documentation:** [Convert Currency](https://exchangeratesapi.io/documentation/#convert-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | yes | Three-letter currency code to convert from. |
| `to` | query | `string` | yes | Three-letter currency code to convert to. |
| `amount` | query | `number` | yes | Amount to convert. |
| `date` | query | `date` | no | Optional historical conversion date in YYYY-MM-DD format. |

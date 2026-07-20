# Convert Amount with Fixer

Converts an amount between currencies in Fixer.

## Endpoint

- **Method:** `GET`
- **Path:** `/convert`
- **Base URL:** `https://data.fixer.io/api`
- **Official documentation:** [Convert Amount](https://fixer.io/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | yes | Three-letter currency code to convert from. |
| `to` | query | `string` | yes | Three-letter currency code to convert to. |
| `amount` | query | `number` | yes | Amount to convert. |
| `date` | query | `string` | no | Optional historical date in YYYY-MM-DD format for historical conversion. |

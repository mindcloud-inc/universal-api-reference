# Convert Currency Amount Using Historical Rates with Currencylayer

Converts a currency amount using historical Currencylayer rates.

## Endpoint

- **Method:** `GET`
- **Path:** `/convert`
- **Base URL:** `https://api.currencylayer.com`
- **Official documentation:** [Convert Currency Amount Using Historical Rates](https://currencylayer.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | yes | 3-letter currency code to convert from. |
| `to` | query | `string` | yes | 3-letter currency code to convert to. |
| `amount` | query | `number` | yes | Amount to convert. |
| `date` | query | `string` | yes | Historical conversion date in YYYY-MM-DD format. |

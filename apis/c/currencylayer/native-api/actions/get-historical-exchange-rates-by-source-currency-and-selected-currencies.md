# Get Historical Exchange Rates By Source Currency And Selected Currencies with Currencylayer

Retrieves historical exchange rates by source and selected currencies from Currencylayer on a date.

## Endpoint

- **Method:** `GET`
- **Path:** `/historical`
- **Base URL:** `https://api.currencylayer.com`
- **Official documentation:** [Get Historical Exchange Rates By Source Currency And Selected Currencies](https://currencylayer.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | yes | Date to retrieve historical rates for, in YYYY-MM-DD format. |
| `source` | query | `string` | yes | 3-letter source currency code. |
| `currencies` | query | `string` | yes | Comma-separated 3-letter currency codes to limit the returned rates. |

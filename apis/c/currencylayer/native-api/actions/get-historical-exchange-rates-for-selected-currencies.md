# Get Historical Exchange Rates For Selected Currencies with Currencylayer

Retrieves historical exchange rates for selected currencies from Currencylayer on a date.

## Endpoint

- **Method:** `GET`
- **Path:** `/historical`
- **Base URL:** `https://api.currencylayer.com`
- **Official documentation:** [Get Historical Exchange Rates For Selected Currencies](https://currencylayer.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | yes | Date to retrieve historical rates for, in YYYY-MM-DD format. |
| `currencies` | query | `string` | yes | Comma-separated 3-letter currency codes to limit the returned rates. |

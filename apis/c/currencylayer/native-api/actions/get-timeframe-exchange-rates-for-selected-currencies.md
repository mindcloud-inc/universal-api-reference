# Get Timeframe Exchange Rates For Selected Currencies with Currencylayer

Retrieves timeframe exchange rates for selected currencies from Currencylayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/timeframe`
- **Base URL:** `https://api.currencylayer.com`
- **Official documentation:** [Get Timeframe Exchange Rates For Selected Currencies](https://currencylayer.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | Start date for the requested timeframe, in YYYY-MM-DD format. |
| `end_date` | query | `string` | yes | End date for the requested timeframe, in YYYY-MM-DD format. |
| `currencies` | query | `string` | yes | Comma-separated 3-letter currency codes to limit the returned rates. |

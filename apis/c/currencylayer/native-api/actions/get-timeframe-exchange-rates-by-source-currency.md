# Get Timeframe Exchange Rates By Source Currency with Currencylayer

Retrieves timeframe exchange rates by source currency from Currencylayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/timeframe`
- **Base URL:** `https://api.currencylayer.com`
- **Official documentation:** [Get Timeframe Exchange Rates By Source Currency](https://currencylayer.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | Start date for the requested timeframe, in YYYY-MM-DD format. |
| `end_date` | query | `string` | yes | End date for the requested timeframe, in YYYY-MM-DD format. |
| `source` | query | `string` | yes | 3-letter source currency code. |

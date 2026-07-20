# Get Timeframe Exchange Rates with Currencylayer

Retrieves exchange rates over a date range from Currencylayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/timeframe`
- **Base URL:** `https://api.currencylayer.com`
- **Official documentation:** [Get Timeframe Exchange Rates](https://currencylayer.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | Start date for the requested timeframe, in YYYY-MM-DD format. |
| `end_date` | query | `string` | yes | End date for the requested timeframe, in YYYY-MM-DD format. |

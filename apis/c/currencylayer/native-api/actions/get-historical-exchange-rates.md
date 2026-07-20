# Get Historical Exchange Rates with Currencylayer

Retrieves historical exchange rates from Currencylayer for a specific date.

## Endpoint

- **Method:** `GET`
- **Path:** `/historical`
- **Base URL:** `https://api.currencylayer.com`
- **Official documentation:** [Get Historical Exchange Rates](https://currencylayer.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | yes | Date to retrieve historical rates for, in YYYY-MM-DD format. |

# Get Currency Change Over Timeframe with Currencylayer

Retrieves currency change data over a timeframe from Currencylayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/change`
- **Base URL:** `https://api.currencylayer.com`
- **Official documentation:** [Get Currency Change Over Timeframe](https://currencylayer.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | Start date for the change calculation, in YYYY-MM-DD format. |
| `end_date` | query | `string` | yes | End date for the change calculation, in YYYY-MM-DD format. |

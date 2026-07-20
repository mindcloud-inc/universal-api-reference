# Get Earnings Calendar with Alpha Vantage

Retrieves earnings calendar data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get Earnings Calendar](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `horizon` | query | `string` | yes | Query parameter $key for EARNINGS_CALENDAR. |
| `symbol` | query | `string` | no | Query parameter $key for EARNINGS_CALENDAR. |

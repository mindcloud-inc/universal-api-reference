# List Earnings Calendar with EODHD

Retrieves earnings calendar events from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/calendar/earnings`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [List Earnings Calendar](https://eodhd.com/financial-apis/calendar-upcoming-earnings-ipos-and-splits/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbols` | query | `string` | no | Comma-separated EODHD tickers. When supplied, from/to are ignored by EODHD. |
| `from` | query | `date` | no | Start date in `YYYY-MM-DD` format. |
| `to` | query | `date` | no | End date in `YYYY-MM-DD` format. |

# List Dividends Calendar with EODHD

Retrieves dividend calendar events from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/calendar/dividends`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [List Dividends Calendar](https://eodhd.com/financial-apis/calendar-upcoming-earnings-ipos-and-splits/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | no | Start date in YYYY-MM-DD format. |
| `to` | query | `date` | no | End date in YYYY-MM-DD format. |

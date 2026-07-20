# List Splits Calendar with EODHD

Retrieves stock split calendar events from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/calendar/splits`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [List Splits Calendar](https://eodhd.com/financial-apis/calendar-upcoming-earnings-ipos-and-splits/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | no | Start date in YYYY-MM-DD format. |
| `to` | query | `date` | no | End date in YYYY-MM-DD format. |

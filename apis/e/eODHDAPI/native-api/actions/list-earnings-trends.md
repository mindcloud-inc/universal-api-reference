# List Earnings Trends with EODHD

Retrieves earnings trends for symbols from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/calendar/trends`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [List Earnings Trends](https://eodhd.com/financial-apis/calendar-upcoming-earnings-ipos-and-splits/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbols` | query | `string` | yes | Comma-separated EODHD tickers for earnings trend lookup. |

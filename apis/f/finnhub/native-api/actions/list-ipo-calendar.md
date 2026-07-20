# List IPO Calendar with Finnhub

Retrieves the IPO calendar from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/calendar/ipo`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [List IPO Calendar](https://finnhub.io/docs/api#ipo-calendar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | yes | Start date in YYYY-MM-DD format. |
| `to` | query | `string` | yes | End date in YYYY-MM-DD format. |

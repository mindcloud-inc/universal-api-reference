# List Earnings Calendar with Finnhub

Retrieves the earnings calendar from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/calendar/earnings`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [List Earnings Calendar](https://finnhub.io/docs/api#earnings-calendar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | Start date in YYYY-MM-DD format. |
| `to` | query | `string` | no | End date in YYYY-MM-DD format. |
| `symbol` | query | `string` | no | Optional company symbol, such as AAPL. |
| `international` | query | `boolean` | no | Set true to include international earnings calendar entries. |

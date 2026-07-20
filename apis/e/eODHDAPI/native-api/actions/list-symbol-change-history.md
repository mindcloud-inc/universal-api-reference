# List Symbol Change History with EODHD

Retrieves stock symbol change history from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/symbol-change-history`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [List Symbol Change History](https://eodhd.com/financial-apis/exchanges-api-trading-hours-and-stock-market-holidays/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | no | Start date in `YYYY-MM-DD` format. |
| `to` | query | `date` | no | End date in `YYYY-MM-DD` format. |

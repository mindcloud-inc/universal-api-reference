# List Economic Events with EODHD

Retrieves economic events from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/economic-events`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [List Economic Events](https://eodhd.com/financial-apis/economic-events-data-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | no | Start date in YYYY-MM-DD format. |
| `to` | query | `date` | no | End date in YYYY-MM-DD format. |
| `country` | query | `string` | no | Country code filter, for example US. |
| `comparison` | query | `string` | no | Optional economic-event comparison filter. |

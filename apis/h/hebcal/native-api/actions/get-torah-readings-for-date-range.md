# Get Torah Readings for Date Range with Hebcal

Retrieves Torah readings for a date range from Hebcal.

## Endpoint

- **Method:** `GET`
- **Path:** `/leyning`
- **Base URL:** `https://www.hebcal.com`
- **Official documentation:** [Get Torah Readings for Date Range](https://www.hebcal.com/home/4277/leyning-torah-reading-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `string` | yes | Gregorian start date in YYYY-MM-DD format. |
| `end` | query | `string` | yes | Gregorian end date in YYYY-MM-DD format. |
| `i` | query | `string` | no | Use Israel Torah reading schedule when enabled. |

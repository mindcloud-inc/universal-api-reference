# List Astronomy Pictures by Date Range with APOD

Retrieves APOD entries from NASA by date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/planetary/apod`
- **Base URL:** `https://api.nasa.gov`
- **Official documentation:** [List Astronomy Pictures by Date Range](https://api.nasa.gov/#apod)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `date` | yes | Start of the APOD date range in YYYY-MM-DD format. |
| `end_date` | query | `date` | no | End of the APOD date range in YYYY-MM-DD format. Defaults to today when omitted. |
| `thumbs` | query | `boolean` | no | Return thumbnail URLs when APOD media entries are videos. |

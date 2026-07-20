# Get Triennial Torah Reading for Date with Hebcal

Retrieves the triennial Torah reading for a date from Hebcal.

## Endpoint

- **Method:** `GET`
- **Path:** `/leyning`
- **Base URL:** `https://www.hebcal.com`
- **Official documentation:** [Get Triennial Torah Reading for Date](https://www.hebcal.com/home/4277/leyning-torah-reading-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | yes | Gregorian date in YYYY-MM-DD format. |
| `i` | query | `string` | no | Use Israel Torah reading schedule when enabled. |

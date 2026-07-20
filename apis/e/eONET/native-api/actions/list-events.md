# List Events with EONET

Retrieves events from EONET.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://eonet.gsfc.nasa.gov/api/v3`
- **Official documentation:** [List Events](https://eonet.gsfc.nasa.gov/docs/v3#events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Event status filter: open, closed, or all. |
| `source` | query | `string` | no | Comma-separated EONET source IDs. |
| `category` | query | `string` | no | Comma-separated EONET category IDs. |
| `days` | query | `number` | no | Number of prior days, including today, to return. |
| `start` | query | `date` | no | Start date in YYYY-MM-DD format. |
| `end` | query | `date` | no | End date in YYYY-MM-DD format. |
| `bbox` | query | `string` | no | Bounding box as min lon, max lat, max lon, min lat. |
| `magID` | query | `string` | no | Filter by magnitude type ID. |
| `magMin` | query | `number` | no | Minimum magnitude value. |
| `magMax` | query | `number` | no | Maximum magnitude value. |

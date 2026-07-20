# List GeoJSON Event Features with EONET

Retrieves GeoJSON event features from EONET.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/geojson`
- **Base URL:** `https://eonet.gsfc.nasa.gov/api/v3`
- **Official documentation:** [List GeoJSON Event Features](https://eonet.gsfc.nasa.gov/docs/v3#events-api-geojson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter events by status: open, closed, or all. |
| `source` | query | `string` | no | Filter by source ID. Comma-separated values act as OR. |
| `category` | query | `string` | no | Filter by category ID. Comma-separated values act as OR. |
| `days` | query | `number` | no | Return events from the last N days, including today. |
| `start` | query | `date` | no | Return events on or after this date (YYYY-MM-DD). |
| `end` | query | `date` | no | Return events on or before this date (YYYY-MM-DD). |
| `bbox` | query | `string` | no | Bounding box as upper-left lon,lat and lower-right lon,lat. |
| `magID` | query | `string` | no | Filter by magnitude type ID. |
| `magMin` | query | `number` | no | Minimum magnitude value. |
| `magMax` | query | `number` | no | Maximum magnitude value. |

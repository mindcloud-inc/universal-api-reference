# List Events for Category with EONET

Retrieves events for a category from EONET.

## Endpoint

- **Method:** `GET`
- **Path:** `/categories/:categoryId`
- **Base URL:** `https://eonet.gsfc.nasa.gov/api/v3`
- **Official documentation:** [List Events for Category](https://eonet.gsfc.nasa.gov/docs/v3#categories-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryId` | path | `string` | yes | Category ID such as wildfires or volcanoes. |
| `source` | query | `string` | no | Filter by source ID. Comma-separated values act as OR. |
| `status` | query | `string` | no | Filter events by status: open, closed, or all. |
| `days` | query | `number` | no | Return events from the last N days, including today. |
| `start` | query | `date` | no | Return events on or after this date (YYYY-MM-DD). |
| `end` | query | `date` | no | Return events on or before this date (YYYY-MM-DD). |

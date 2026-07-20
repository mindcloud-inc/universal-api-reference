# Export Hourly Data JSON with Simple Analytics

Exports hourly data from Simple Analytics in JSON.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/export/datapoints`
- **Base URL:** `https://simpleanalytics.com`
- **Official documentation:** [Export Hourly Data JSON](https://docs.simpleanalytics.com/api/export-data-points)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `hostname` | query | `string` | yes |
| `start` | query | `string` | yes |
| `end` | query | `string` | yes |
| `fields` | query | `string` | yes |
| `type` | query | `string` | yes |

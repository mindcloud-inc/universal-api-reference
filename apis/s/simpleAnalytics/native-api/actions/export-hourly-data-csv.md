# Export Hourly Data CSV with Simple Analytics

Exports hourly data from Simple Analytics in CSV.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/export/datapoints`
- **Base URL:** `https://simpleanalytics.com`
- **Official documentation:** [Export Hourly Data CSV](https://docs.simpleanalytics.com/api/export-data-points)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `hostname` | query | `string` | yes |
| `start` | query | `string` | yes |
| `end` | query | `string` | yes |
| `fields` | query | `string` | yes |
| `type` | query | `string` | yes |

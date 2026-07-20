# List Metrics By Country with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/site-explorer/metrics-by-country`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [List Metrics By Country](https://docs.ahrefs.com/en/api/reference/site-explorer/get-metrics-by-country)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Domain or URL to analyze. |
| `date` | query | `date` | yes | Date to report metrics on in YYYY-MM-DD format. |

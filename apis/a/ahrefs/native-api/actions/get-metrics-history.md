# Get Metrics History with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/site-explorer/metrics-history`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [Get Metrics History](https://docs.ahrefs.com/en/api/reference/site-explorer/get-metrics-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Domain or URL to analyze. |
| `date_from` | query | `date` | yes | Start date in YYYY-MM-DD format. |
| `date_to` | query | `date` | no | End date in YYYY-MM-DD format. |

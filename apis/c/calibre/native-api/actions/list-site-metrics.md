# List Site Metrics with Calibre

Retrieves timeseries metrics for a site from Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [List Site Metrics](https://calibreapp.com/docs/automation/retrieving-metrics#timeseries-metrics-for-a-given-site)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.site` | body | `string` | yes | Site slug, found in site settings. |
| `variables.measurement` | body | `string` | no | Metric tag to retrieve for the site. |

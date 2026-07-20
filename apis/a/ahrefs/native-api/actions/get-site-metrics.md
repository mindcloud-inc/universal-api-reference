# Get Site Metrics with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/site-explorer/metrics`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [Get Site Metrics](https://docs.ahrefs.com/en/api/reference/site-explorer/get-metrics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | Two-letter ISO 3166-1 alpha-2 country code. |
| `target` | query | `string` | yes | Domain or URL to analyze. |
| `date` | query | `date` | yes | Report date in YYYY-MM-DD format. |
| `mode` | query | `string` | no | Target scope: exact, prefix, domain, or subdomains. |
| `volume_mode` | query | `string` | no | Search volume calculation mode: monthly or average. |

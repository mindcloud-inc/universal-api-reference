# List Organic Competitors with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/site-explorer/organic-competitors`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [List Organic Competitors](https://docs.ahrefs.com/en/api/reference/site-explorer/get-organic-competitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Domain or URL to analyze. |
| `date` | query | `date` | yes | Report date in YYYY-MM-DD format. |
| `country` | query | `string` | yes | Two-letter ISO 3166-1 alpha-2 country code. |
| `select` | query | `string` | yes | Comma-separated competitor columns to return. |

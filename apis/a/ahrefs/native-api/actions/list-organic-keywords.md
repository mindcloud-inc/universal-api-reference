# List Organic Keywords with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/site-explorer/organic-keywords`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [List Organic Keywords](https://docs.ahrefs.com/en/api/reference/site-explorer/get-organic-keywords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Domain or URL to analyze. |
| `date` | query | `date` | yes | Report date in YYYY-MM-DD format. |
| `select` | query | `string` | yes | Comma-separated organic keyword columns to return. |

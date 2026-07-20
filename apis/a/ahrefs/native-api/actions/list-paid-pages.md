# List Paid Pages with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/site-explorer/paid-pages`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [List Paid Pages](https://docs.ahrefs.com/en/api/reference/site-explorer/get-paid-pages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Domain or URL to analyze. |
| `date` | query | `date` | yes | Report date in YYYY-MM-DD format. |
| `select` | query | `string` | yes | Comma-separated paid-page columns to return. |

# List Top Pages with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/site-explorer/top-pages`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [List Top Pages](https://docs.ahrefs.com/en/api/reference/site-explorer/get-top-pages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Domain or URL to analyze. |
| `date` | query | `date` | yes | Report date in YYYY-MM-DD format. |
| `select` | query | `string` | yes | Comma-separated top-page columns to return. |

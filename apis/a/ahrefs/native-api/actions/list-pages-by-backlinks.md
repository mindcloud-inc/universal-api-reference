# List Pages By Backlinks with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/site-explorer/pages-by-backlinks`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [List Pages By Backlinks](https://docs.ahrefs.com/en/api/reference/site-explorer/get-pages-by-backlinks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Domain or URL to analyze. |
| `select` | query | `string` | yes | Comma-separated page backlink columns to return. |

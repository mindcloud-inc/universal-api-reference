# List Backlinks with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/site-explorer/all-backlinks`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [List Backlinks](https://docs.ahrefs.com/en/api/reference/site-explorer/get-all-backlinks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mode` | query | `string` | no | Target scope: exact, prefix, domain, or subdomains. |
| `target` | query | `string` | yes | Domain or URL to analyze. |
| `select` | query | `string` | yes | Comma-separated backlink columns to return. |

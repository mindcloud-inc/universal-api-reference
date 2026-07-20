# Get Backlinks Stats with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/site-explorer/backlinks-stats`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [Get Backlinks Stats](https://docs.ahrefs.com/en/api/reference/site-explorer/get-backlinks-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mode` | query | `string` | no | Target scope: exact, prefix, domain, or subdomains. |
| `target` | query | `string` | yes | Domain or URL to analyze. |
| `date` | query | `date` | yes | Report date in YYYY-MM-DD format. |

# List Referring Domains with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/site-explorer/refdomains`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [List Referring Domains](https://docs.ahrefs.com/en/api/reference/site-explorer/get-refdomains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Domain or URL to analyze. |
| `select` | query | `string` | yes | Comma-separated referring-domain columns to return. |

# List Linked Domains with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/site-explorer/linkeddomains`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [List Linked Domains](https://docs.ahrefs.com/en/api/reference/site-explorer/get-linkeddomains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Domain or URL to analyze. |
| `select` | query | `string` | yes | Comma-separated linked-domain columns to return. |

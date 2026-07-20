# List Anchors with Ahrefs

## Endpoint

- **Method:** `GET`
- **Path:** `/site-explorer/anchors`
- **Base URL:** `https://api.ahrefs.com/v3`
- **Official documentation:** [List Anchors](https://docs.ahrefs.com/en/api/reference/site-explorer/get-anchors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Domain or URL to analyze. |
| `select` | query | `string` | yes | Comma-separated anchor columns to return. |

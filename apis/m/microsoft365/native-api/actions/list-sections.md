# List Sections with Microsoft 365

Retrieves OneNote sections from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/onenote/sections`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [List Sections](https://learn.microsoft.com/en-us/graph/api/onenote-list-sections?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Maximum number of sections to return. |

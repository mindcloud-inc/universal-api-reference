# List Pages with Microsoft 365

Retrieves OneNote pages from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/onenote/pages`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [List Pages](https://learn.microsoft.com/en-us/graph/api/onenote-list-pages?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Maximum number of pages to return. |

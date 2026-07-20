# Get Page with Microsoft 365

Retrieves a OneNote page from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/onenote/pages/{{pageId}}`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Get Page](https://learn.microsoft.com/en-us/graph/api/page-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | The OneNote page ID. |

# Create Section with Microsoft 365

Creates a new section in Microsoft 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/onenote/notebooks/{{notebookId}}/sections`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Create Section](https://learn.microsoft.com/en-us/graph/api/notebook-post-sections?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notebookId` | path | `string` | yes | The target notebook ID. |
| `displayName` | body | `string` | yes | The section name to create. |

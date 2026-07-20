# Create Notebook with Microsoft 365

Creates a new notebook in Microsoft 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/onenote/notebooks`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Create Notebook](https://learn.microsoft.com/en-us/graph/api/onenote-post-notebooks?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `displayName` | body | `string` | yes | The notebook name to create. |

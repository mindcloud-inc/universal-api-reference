# List Notebooks with Microsoft 365

Retrieves notebooks from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/onenote/notebooks`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [List Notebooks](https://learn.microsoft.com/en-us/graph/api/onenote-list-notebooks?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Maximum number of notebooks to return. |

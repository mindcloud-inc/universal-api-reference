# List Entra Groups with Microsoft 365

Retrieves Entra groups from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/groups`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (nextLink pagination)
- **Official documentation:** [List Entra Groups](https://learn.microsoft.com/en-us/graph/api/group-list?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | User OData filters on the dataset |

# List Entra Group Users with Microsoft 365

Retrieves Entra group members from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/groups/:id/members`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (nextLink pagination)
- **Official documentation:** [List Entra Group Users](https://learn.microsoft.com/en-us/graph/api/group-list?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | User OData filters on the dataset |
| `id` | path | `string` | yes | — |

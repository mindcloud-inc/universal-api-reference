# List Entra Users with Microsoft 365

Retrieves Entra users from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/users`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (nextLink pagination)
- **Official documentation:** [List Entra Users](https://learn.microsoft.com/en-us/graph/api/user-list?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | OData filter |
| `$select` | query | `string` | no | OData select |
| `$expand` | query | `string` | no | OData expand |

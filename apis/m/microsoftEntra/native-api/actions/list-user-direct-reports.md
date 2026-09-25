# List User Direct Reports with Microsoft Entra

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:userId/directReports`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [List User Direct Reports](https://learn.microsoft.com/en-us/graph/api/user-list-directreports?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The user's ID or user principal name. |
| `$select` | query | `string` | no | Comma-separated properties to return. |
| `$expand` | query | `string` | no | An OData expansion expression. |
| `$filter` | query | `string` | no | An OData filter expression; some queries require Include Count. |
| `$count` | query | `boolean` | no | Include a count for advanced directory queries. |

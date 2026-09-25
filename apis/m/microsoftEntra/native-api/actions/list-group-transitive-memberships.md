# List Group Transitive Memberships with Microsoft Entra

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:groupId/transitiveMemberOf`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [List Group Transitive Memberships](https://learn.microsoft.com/en-us/graph/api/group-list-transitivememberof?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | OData filter expression; requires Include Count. |
| `groupId` | path | `list<string>` | yes | — |
| `$search` | query | `string` | no | Search displayName or description; requires Include Count. |
| `$select` | query | `string` | no | Comma-separated property names. |
| `$count` | query | `boolean` | no | Required for advanced directory queries. |

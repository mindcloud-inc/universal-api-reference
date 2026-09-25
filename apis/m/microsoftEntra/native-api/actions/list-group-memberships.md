# List Group Memberships with Microsoft Entra

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:groupId/memberOf`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [List Group Memberships](https://learn.microsoft.com/en-us/graph/api/group-list-memberof?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | OData filter expression; requires Include Count. |
| `groupId` | path | `list<string>` | yes | — |
| `$search` | query | `string` | no | Search displayName or description; requires Include Count. |
| `$select` | query | `string` | no | Comma-separated property names. |
| `$count` | query | `boolean` | no | Required for advanced directory queries. |

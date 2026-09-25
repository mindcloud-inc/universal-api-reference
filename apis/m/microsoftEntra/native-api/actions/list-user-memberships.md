# List User Memberships with Microsoft Entra

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:userId/memberOf`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [List User Memberships](https://learn.microsoft.com/en-us/graph/api/user-list-memberof?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `list<string>` | yes | — |
| `$select` | query | `string` | no | Comma-separated properties, such as id,displayName. |
| `$filter` | query | `string` | no | OData filter expression. Advanced queries require Include Count. |
| `$search` | query | `string` | no | Search expression, such as "displayName:Ava". Requires Include Count. |
| `$count` | query | `boolean` | no | Include the matching count. Required for advanced search, filtering, and sorting. |

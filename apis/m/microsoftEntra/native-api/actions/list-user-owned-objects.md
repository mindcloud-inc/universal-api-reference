# List User Owned Objects with Microsoft Entra

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:userId/ownedObjects`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [List User Owned Objects](https://learn.microsoft.com/en-us/graph/api/user-list-ownedobjects?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$select` | query | `string` | no | Comma-separated properties, such as id,displayName. |
| `userId` | path | `list<string>` | yes | — |

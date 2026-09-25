# Get User Manager with Microsoft Entra

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:userId/manager`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Get User Manager](https://learn.microsoft.com/en-us/graph/api/user-list-manager?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The user's ID or user principal name. |
| `$select` | query | `string` | no | Comma-separated properties to return. |
| `$expand` | query | `string` | no | An OData expansion expression. |

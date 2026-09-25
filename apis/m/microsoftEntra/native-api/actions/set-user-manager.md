# Set User Manager with Microsoft Entra

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:userId/manager/$ref`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Set User Manager](https://learn.microsoft.com/en-us/graph/api/user-post-manager?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The user's ID or user principal name. |
| `@odata.id` | body | `string` | yes | The Microsoft Graph read URL of the manager, for example https://graph.microsoft.com/v1.0/users/{managerId}. |

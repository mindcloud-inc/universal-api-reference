# Remove User Manager with Microsoft Entra

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/:userId/manager/$ref`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Remove User Manager](https://learn.microsoft.com/en-us/graph/api/user-delete-manager?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The user's ID or user principal name. |

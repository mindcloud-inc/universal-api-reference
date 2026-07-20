# Remove Manager Role from User with Clockify

Removes the manager role from a user in Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/users/:userId/roles`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Remove Manager Role from User](https://docs.developer.clockify.me/#tag/User/operation/deleteUserRole)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `userId` | path | `string<string>` | yes | — |
| `entityId` | body | `string` | yes | — |
| `role` | body | `list<string>` | yes | Accepted values: `PROJECT_MANAGER`, `TEAM_MANAGER`, `WORKSPACE_ADMIN`. |
| `sourceType` | body | `list<string>` | no | Accepted values: `USER_GROUP`. |

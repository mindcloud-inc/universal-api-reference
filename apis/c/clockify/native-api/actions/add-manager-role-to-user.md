# Add Manager Role to User with Clockify

Adds the manager role to a user in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/users/:userId/roles`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Add Manager Role to User](https://docs.developer.clockify.me/#tag/User/operation/createUserRole)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `userId` | path | `string<string>` | yes | — |
| `entityId` | body | `string` | yes | — |
| `role` | body | `list<string>` | yes | Accepted values: `PROJECT_MANAGER`, `TEAM_MANAGER`, `WORKSPACE_ADMIN`. |
| `sourceType` | body | `list<string>` | no | Accepted values: `USER_GROUP`. |

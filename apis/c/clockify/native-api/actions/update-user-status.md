# Update User Status with Clockify

Updates a user status in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/users/:userId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update User Status](https://docs.developer.clockify.me/#tag/Workspace/operation/updateUserStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `userId` | path | `string<string>` | yes | — |
| `status` | body | `list<string>` | yes | Accepted values: `ACTIVE`, `INACTIVE`. |

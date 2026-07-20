# List User Managers with Clockify

Lists all user managers in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/users/:userId/managers`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List User Managers](https://docs.developer.clockify.me/#tag/User/operation/getManagersOfUser)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `userId` | path | `string<string>` | yes |

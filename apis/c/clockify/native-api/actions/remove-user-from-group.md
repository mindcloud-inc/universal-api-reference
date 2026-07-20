# Remove User from Group with Clockify

Removes a user from a group in Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/user-groups/:userGroupId/users/:userId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Remove User from Group](https://docs.developer.clockify.me/#tag/Group/operation/deleteUser)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `userGroupId` | path | `string` | yes |
| `userId` | path | `string` | yes |
| `workspaceId` | path | `list<string>` | yes |

# Add User To Group with Reach360

Adds a user to a Reach360 group.

## Endpoint

- **Method:** `PUT`
- **Path:** `/groups/:groupId/users/:userId`
- **Base URL:** `https://api.reach360.com`
- **Official documentation:** [Add User To Group](https://www.articulatesupport.com/article/Reach-360-Group-Memberships-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The group ID. |
| `userId` | path | `string` | yes | The user ID. |

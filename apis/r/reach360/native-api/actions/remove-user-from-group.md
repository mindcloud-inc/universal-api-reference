# Remove User From Group with Reach360

Removes a user from a Reach360 group.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/groups/:groupId/users/:userId`
- **Base URL:** `https://api.reach360.com`
- **Official documentation:** [Remove User From Group](https://www.articulatesupport.com/article/Reach-360-Group-Memberships-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The group ID. |
| `userId` | path | `string` | yes | The user ID. |

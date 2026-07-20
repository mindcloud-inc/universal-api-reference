# List User Groups with Reach360

Retrieves all groups for a Reach360 user.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:userId/groups`
- **Base URL:** `https://api.reach360.com`
- **Official documentation:** [List User Groups](https://www.articulatesupport.com/article/Reach-360-Group-Memberships-API)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The user ID. |

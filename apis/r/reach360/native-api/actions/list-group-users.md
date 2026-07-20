# List Group Users with Reach360

Retrieves all users in a Reach360 group.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:groupId/users`
- **Base URL:** `https://api.reach360.com`
- **Official documentation:** [List Group Users](https://www.articulatesupport.com/article/Reach-360-Group-Memberships-API)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The group ID. |

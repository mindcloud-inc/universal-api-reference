# Update Group with Reach360

Updates an existing group in Reach360.

## Endpoint

- **Method:** `PUT`
- **Path:** `/groups/:groupId`
- **Base URL:** `https://api.reach360.com`
- **Official documentation:** [Update Group](https://www.articulatesupport.com/article/Reach-360-Groups-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The group ID. |
| `name` | body | `string` | yes | The group name. |

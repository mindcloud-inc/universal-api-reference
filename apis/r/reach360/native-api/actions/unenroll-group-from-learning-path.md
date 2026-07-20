# Unenroll Group From Learning Path with Reach360

Removes a group from a Reach360 learning path.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/learning-paths/:learningPathId/groups/:groupId`
- **Base URL:** `https://api.reach360.com`
- **Official documentation:** [Unenroll Group From Learning Path](https://www.articulatesupport.com/article/Reach-360-Learning-Path-Enrollments-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `learningPathId` | path | `string` | yes | The learning path ID. |
| `groupId` | path | `string` | yes | The group ID. |

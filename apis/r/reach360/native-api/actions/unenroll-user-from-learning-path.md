# Unenroll User From Learning Path with Reach360

Removes a user from a Reach360 learning path.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/learning-paths/:learningPathId/users/:userId`
- **Base URL:** `https://api.reach360.com`
- **Official documentation:** [Unenroll User From Learning Path](https://www.articulatesupport.com/article/Reach-360-Learning-Path-Enrollments-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `learningPathId` | path | `string` | yes | The learning path ID. |
| `userId` | path | `string` | yes | The user ID. |

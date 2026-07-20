# Enroll User In Learning Path with Reach360

Enrolls a user in a Reach360 learning path.

## Endpoint

- **Method:** `PUT`
- **Path:** `/learning-paths/:learningPathId/users/:userId`
- **Base URL:** `https://api.reach360.com`
- **Official documentation:** [Enroll User In Learning Path](https://www.articulatesupport.com/article/Reach-360-Learning-Path-Enrollments-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `learningPathId` | path | `string` | yes | The learning path ID. |
| `userId` | path | `string` | yes | The user ID. |

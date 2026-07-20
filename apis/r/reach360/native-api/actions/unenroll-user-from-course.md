# Unenroll User From Course with Reach360

Removes a user from a Reach360 course.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/courses/:courseId/users/:userId`
- **Base URL:** `https://api.reach360.com`
- **Official documentation:** [Unenroll User From Course](https://www.articulatesupport.com/article/Reach-360-Course-Enrollments-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `courseId` | path | `string` | yes | The course ID. |
| `userId` | path | `string` | yes | The user ID. |

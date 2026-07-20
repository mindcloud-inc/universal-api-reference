# Enroll User In Course with Reach360

Enrolls a user in a Reach360 course.

## Endpoint

- **Method:** `PUT`
- **Path:** `/courses/:courseId/users/:userId`
- **Base URL:** `https://api.reach360.com`
- **Official documentation:** [Enroll User In Course](https://www.articulatesupport.com/article/Reach-360-Course-Enrollments-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `courseId` | path | `string` | yes | The course ID. |
| `userId` | path | `string` | yes | The user ID. |

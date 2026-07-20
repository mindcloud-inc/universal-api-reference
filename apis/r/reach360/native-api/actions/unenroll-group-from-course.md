# Unenroll Group From Course with Reach360

Removes a group from a Reach360 course.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/courses/:courseId/groups/:groupId`
- **Base URL:** `https://api.reach360.com`
- **Official documentation:** [Unenroll Group From Course](https://www.articulatesupport.com/article/Reach-360-Course-Enrollments-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `courseId` | path | `string` | yes | The course ID. |
| `groupId` | path | `string` | yes | The group ID. |

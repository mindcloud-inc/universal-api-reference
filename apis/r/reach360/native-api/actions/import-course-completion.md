# Import Course Completion with Reach360

Imports a user's course completion into Reach360.

## Endpoint

- **Method:** `POST`
- **Path:** `/courses/:courseId/users/:userId/completions`
- **Base URL:** `https://api.reach360.com`
- **Official documentation:** [Import Course Completion](https://www.articulatesupport.com/article/Reach-360-Import-Course-Completion-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `courseId` | path | `string` | yes | The course ID. |
| `userId` | path | `string` | yes | The user ID. |
| `startedAt` | body | `date` | yes | When the user started the course. |
| `completedAt` | body | `date` | yes | When the user completed the course. |

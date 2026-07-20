# Set Task Assignees with Awork

Updates task assignees in Awork.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/setassignees`
- **Base URL:** `https://api.awork.com/api/v1`
- **Official documentation:** [Set Task Assignees](https://developers.awork.com/apiv1/tasks/post-set-assignees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The id of the task. |
| `userIds[]` | body | `array<string>` | yes | Array of user IDs to assign to the task. This replaces the existing assignee list. |

# Update Task Assignments with CheckFlow

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/task/assignments`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Update Task Assignments](https://docs.checkflow.io/docs/api/tasks#update-task-assignments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskID` | body | `number` | yes | The ID of the task to update assignees for. |
| `assignees[]` | body | `array<object>` | yes | The assignee objects to set on the task. |
| `assignees[].assigneeId` | body | `number` | yes | The member or group ID. |
| `assignees[].assigneeType` | body | `number` | yes | The assignee type. Use 1 for member and 2 for group. |
| `assignees[].assigneeName` | body | `string` | no | The display name of the assignee. |
| `isAssignedExclusively` | body | `boolean` | yes | Whether the provided assignees should become the exclusive assignees. |

# Add Task Assignees by Name with CheckFlow

## Endpoint

- **Method:** `POST`
- **Path:** `/api/task/assign-by-name`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Add Task Assignees by Name](https://docs.checkflow.io/docs/api/tasks#add-task-assignees-by-name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskID` | body | `number` | yes | The ID of the task to update assignees for. |
| `assigneeNames[]` | body | `array<string>` | yes | The member or group names to assign to the task. |
| `isAssignedExclusively` | body | `boolean` | yes | Whether the named assignees should replace any other candidates for assignment selection. |
| `deleteExistingAssignees` | body | `boolean` | yes | Whether existing assignees should be removed before adding the new names. |

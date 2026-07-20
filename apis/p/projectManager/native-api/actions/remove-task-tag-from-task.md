# Remove TaskTag from Task with ProjectManager

Removes a task tag from a task in ProjectManager.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/data/tasks/:taskId/tags`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Remove TaskTag from Task](https://developer.projectmanager.com/api-reference/task-tag/remove-task-tag-from-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The unique identifier of the Task for which we will remove existing TaskTags |
| `value[]` | body | `array` | yes | — |
| `value[]` | body | `array` | yes | — |
| `value[]` | body | `array` | yes | — |
| `value[]` | body | `array` | yes | — |

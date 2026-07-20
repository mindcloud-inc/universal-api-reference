# Add TaskTag to Task with ProjectManager

Adds a task tag to a task in ProjectManager.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/data/tasks/:taskId/tags`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Add TaskTag to Task](https://developer.projectmanager.com/api-reference/task-tag/add-task-tag-to-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The unique identifier of the Task for which we will add TaskTags |
| `value[]` | body | `array` | yes | — |
| `value[]` | body | `array` | yes | — |
| `value[]` | body | `array` | yes | — |
| `value[]` | body | `array` | yes | — |

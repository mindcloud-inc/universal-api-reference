# Fetch the first level child tasks from the task with ProjectManager

Retrieves first-level subtasks from a task in ProjectManager.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/data/tasks/:taskId/subtasks`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Fetch the first level child tasks from the task](https://developer.projectmanager.com/api-reference/task/fetch-the-first-level-child-tasks-from-the-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Parent task id |

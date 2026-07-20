# Returns task assignees with ProjectManager

Retrieves task assignees from ProjectManager.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/data/tasks/:taskId/assignees`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Returns task assignees](https://developer.projectmanager.com/api-reference/task-assignee/returns-task-assignees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The unique identifier of the Task |

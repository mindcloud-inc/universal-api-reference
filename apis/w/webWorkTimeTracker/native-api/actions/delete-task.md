# Delete Task with WebWork Time Tracker

Deletes an existing task from WebWork Time Tracker.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Delete Task](https://api-docs.webwork-tracker.com/api/tasks/deletetask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `taskId` | path | `number` | yes |
| `workspace_id` | body | `number` | yes |
| `project_id` | body | `number` | yes |

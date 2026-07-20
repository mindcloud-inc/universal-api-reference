# Get Task with WebWork Time Tracker

Retrieves a task from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Get Task](https://api-docs.webwork-tracker.com/api/tasks/gettask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `taskId` | path | `number` | yes |
| `workspace_id` | query | `number` | yes |
| `project_id` | query | `number` | yes |

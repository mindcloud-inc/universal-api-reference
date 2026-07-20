# List Task Assignees with WebWork Time Tracker

Retrieves task assignees from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:taskId/assignees`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [List Task Assignees](https://api-docs.webwork-tracker.com/api/tasks/gettaskassignees)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `taskId` | path | `number` | yes |
| `workspace_id` | query | `number` | yes |
| `project_id` | query | `number` | yes |

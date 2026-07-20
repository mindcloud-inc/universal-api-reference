# Update Task with WebWork Time Tracker

Updates an existing task in WebWork Time Tracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Update Task](https://api-docs.webwork-tracker.com/api/tasks/updatetask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `taskId` | path | `number` | yes |
| `workspace_id` | body | `number` | yes |
| `project_id` | body | `number` | yes |
| `title` | body | `string` | no |
| `description` | body | `string` | no |
| `status` | body | `number` | no |
| `priority` | body | `number` | no |
| `start_date` | body | `date` | no |
| `end_date` | body | `date` | no |
| `parent_id` | body | `number` | no |

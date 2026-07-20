# Create Task with WebWork Time Tracker

Creates a new task in WebWork Time Tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Create Task](https://api-docs.webwork-tracker.com/api/tasks/createtask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes |
| `project_id` | body | `number` | yes |
| `title` | body | `string` | yes |
| `description` | body | `string` | no |
| `status` | body | `number` | no |
| `priority` | body | `number` | no |
| `start_date` | body | `date` | no |
| `end_date` | body | `date` | no |
| `parent_id` | body | `number` | no |

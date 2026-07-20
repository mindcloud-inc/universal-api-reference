# Update Task with BugHerd

Updates an existing task in BugHerd.

## Endpoint

- **Method:** `PUT`
- **Path:** `projects/:project_id/tasks/:task_id.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Update Task](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The BugHerd project ID. |
| `task_id` | path | `number` | yes | The BugHerd task ID. |
| `task` | body | `object` | no | Task fields to update. |
| `task.priority` | body | `string` | no | The BugHerd task priority. |
| `task.status` | body | `string` | no | The target task status or column name. |
| `task.assigned_to_id` | body | `number` | no | Assign the task to a BugHerd user ID. |
| `task.updater_email` | body | `string` | no | Audit-log the update as this email address. |
| `task.unassign_user` | body | `number` | no | Unassign a specific user ID from the task. |

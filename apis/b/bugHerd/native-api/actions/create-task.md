# Create Task with BugHerd

Creates a new task in BugHerd.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_id/tasks.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Create Task](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `task` | body | `object` | no |
| `task.description` | body | `string` | yes |
| `task.priority` | body | `string` | no |
| `task.status` | body | `string` | no |
| `task.assigned_to_id` | body | `number` | no |
| `task.requester_email` | body | `string` | no |
| `task.external_id` | body | `string` | no |

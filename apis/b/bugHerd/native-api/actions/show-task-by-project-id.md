# Show Task By Project ID with BugHerd

Retrieves a task from a BugHerd project.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:project_id/tasks/:task_id.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Show Task By Project ID](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `task_id` | path | `number` | yes |

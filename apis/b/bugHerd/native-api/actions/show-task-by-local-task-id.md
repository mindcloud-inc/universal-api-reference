# Show Task By Local Task ID with BugHerd

Retrieves a BugHerd task by local task ID.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:project_id/local_tasks/:local_task_id.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Show Task By Local Task ID](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `local_task_id` | path | `number` | yes |
| `project_id` | path | `number` | yes |

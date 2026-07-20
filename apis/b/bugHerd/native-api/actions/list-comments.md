# List Comments with BugHerd

Retrieves comments from a BugHerd task.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:project_id/tasks/:task_id/comments.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [List Comments](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The BugHerd project ID. |
| `task_id` | path | `number` | yes | The BugHerd task ID. |

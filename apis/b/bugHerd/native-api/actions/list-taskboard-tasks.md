# List Taskboard Tasks with BugHerd

Retrieves taskboard tasks from a BugHerd project.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:project_id/tasks/taskboard.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [List Taskboard Tasks](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |

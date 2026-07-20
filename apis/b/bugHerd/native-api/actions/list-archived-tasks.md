# List Archived Tasks with BugHerd

Retrieves archived tasks from a BugHerd project.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:project_id/tasks/archive.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [List Archived Tasks](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |

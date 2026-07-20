# List Attachments with BugHerd

Retrieves attachments from a BugHerd task.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:project_id/tasks/:task_id/attachments.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [List Attachments](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The BugHerd project ID. |
| `task_id` | path | `number` | yes | The BugHerd task ID. |

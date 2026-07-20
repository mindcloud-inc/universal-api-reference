# Delete Attachment with BugHerd

Deletes an attachment from a BugHerd task.

## Endpoint

- **Method:** `DELETE`
- **Path:** `projects/:project_id/tasks/:task_id/attachments/:id.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Delete Attachment](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The BugHerd project ID. |
| `task_id` | path | `number` | yes | The BugHerd task ID. |
| `id` | path | `number` | yes | The BugHerd attachment ID. |

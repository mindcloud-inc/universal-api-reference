# Upload Attachment with BugHerd

Uploads an attachment to a BugHerd task.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_id/tasks/:task_id/attachments/upload`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Upload Attachment](https://docs.bugherd.com/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/binary` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `task_id` | path | `number` | yes |
| `file_name` | query | `string` | yes |

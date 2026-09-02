# Create Task Attachment with ClickUp

Uploads a file attachment to a ClickUp task.

## Endpoint

- **Method:** `POST`
- **Path:** `task/:task_id/attachment`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [Create Task Attachment](https://developer.clickup.com/reference/createtaskattachment)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `custom_task_ids` | query | `boolean` | no |
| `task_id` | path | `string` | yes |
| `team_id` | query | `list` | no |
| `attachment` | body | `file` | yes |

# Create Attachment From URL with BugHerd

Creates a task attachment from a URL in BugHerd.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_id/tasks/:task_id/attachments.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Create Attachment From URL](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `task_id` | path | `number` | yes |
| `attachment` | body | `object` | no |
| `attachment.file_name` | body | `string` | yes |
| `attachment.url` | body | `string` | yes |

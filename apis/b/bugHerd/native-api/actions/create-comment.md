# Create Comment with BugHerd

Creates a comment on a BugHerd task.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_id/tasks/:task_id/comments.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Create Comment](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `task_id` | path | `number` | yes |
| `comment` | body | `object` | no |
| `comment.text` | body | `string` | yes |
| `comment.email` | body | `string` | no |
| `comment.user_id` | body | `number` | no |
| `comment.is_private` | body | `boolean` | no |

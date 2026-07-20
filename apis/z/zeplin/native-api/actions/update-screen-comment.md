# Update Screen Comment with Zeplin

Updates an existing screen comment in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/{project_id}/screens/{screen_id}/notes/{note_id}/comments/{comment_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Screen Comment](https://docs.zeplin.dev/reference/updatescreencomment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `screen_id` | path | `string` | yes | Screen id |
| `note_id` | path | `string` | yes | Screen note id |
| `comment_id` | path | `string` | yes | Screen comment id |
| `content` | body | `string` | yes | Content of the comment |

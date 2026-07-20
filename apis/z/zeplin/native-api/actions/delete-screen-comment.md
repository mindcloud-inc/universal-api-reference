# Delete Screen Comment with Zeplin

Deletes an existing screen comment from Zeplin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/{project_id}/screens/{screen_id}/notes/{note_id}/comments/{comment_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Delete Screen Comment](https://docs.zeplin.dev/reference/deletescreencomment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `screen_id` | path | `string` | yes | Screen id |
| `note_id` | path | `string` | yes | Screen note id |
| `comment_id` | path | `string` | yes | Screen comment id |

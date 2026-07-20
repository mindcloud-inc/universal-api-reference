# Create Screen Comment with Zeplin

Creates a new screen comment in Zeplin.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{project_id}/screens/{screen_id}/notes/{note_id}/comments`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Create Screen Comment](https://docs.zeplin.dev/reference/createscreencomment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `screen_id` | path | `string` | yes | Screen id |
| `note_id` | path | `string` | yes | Screen note id |
| `content` | body | `string` | yes | Content of the comment |

# Update Screen Note with Zeplin

Updates an existing screen note in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/{project_id}/screens/{screen_id}/notes/{note_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Screen Note](https://docs.zeplin.dev/reference/updatescreennote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `screen_id` | path | `string` | yes | Screen id |
| `note_id` | path | `string` | yes | Screen note id |
| `status` | body | `string` | yes | Status of the note |
| `position` | body | `object` | yes | Position of the note with respect to top left corner. Values are normalized in [0, 1] |
| `color` | body | `string` | yes | — |

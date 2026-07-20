# Get Screen Note with Zeplin

Retrieves a screen note from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/screens/{screen_id}/notes/{note_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get Screen Note](https://docs.zeplin.dev/reference/getscreennote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `screen_id` | path | `string` | yes | Screen id |
| `note_id` | path | `string` | yes | Screen note id |

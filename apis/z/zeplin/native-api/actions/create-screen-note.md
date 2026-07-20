# Create Screen Note with Zeplin

Creates a new screen note in Zeplin.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{project_id}/screens/{screen_id}/notes`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Create Screen Note](https://docs.zeplin.dev/reference/createscreennote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `screen_id` | path | `string` | yes | Screen id |
| `content` | body | `string` | yes | Content of the first comment of the note |
| `position` | body | `object` | yes | Position of the note with respect to top left corner. Values are normalized in [0, 1] |
| `color` | body | `string` | yes | — |

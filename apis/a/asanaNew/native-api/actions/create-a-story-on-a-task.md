# Create a story on a task with Asana

Creates a story on a task in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks/:task_gid/stories`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a story on a task](https://developers.asana.com/reference/createstoryfortask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.text` | body | `string` | no | The plain text of the comment to add. |
| `task_gid` | path | `string` | yes | — |
| `data` | body | `object` | no | — |

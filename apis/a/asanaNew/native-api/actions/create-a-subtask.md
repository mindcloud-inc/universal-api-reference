# Create a subtask with Asana

Creates a subtask in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks/:task_gid/subtasks`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a subtask](https://developers.asana.com/reference/createsubtaskfortask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_fields[]` | query | `array<string>` | no | — |
| `task_gid` | path | `string` | yes | Path parameter: task_gid |
| `data` | body | `object` | yes | — |

# Set dependents for a task with Asana

Sets dependents for a task in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks/:task_gid/addDependents`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Set dependents for a task](https://developers.asana.com/reference/adddependentsfortask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | — |
| `data.dependents[]` | body | `array<string>` | yes | — |
| `task_gid` | path | `string` | yes | Path parameter: task_gid |

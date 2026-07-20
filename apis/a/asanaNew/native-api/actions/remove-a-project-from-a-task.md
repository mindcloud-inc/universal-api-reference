# Remove a project from a task with Asana

Removes a project from a task in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `tasks/:task_gid/removeProject`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Remove a project from a task](https://developers.asana.com/reference/removeprojectfortask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | — |
| `data.project` | body | `string` | yes | — |
| `task_gid` | path | `string` | yes | Path parameter: task_gid |

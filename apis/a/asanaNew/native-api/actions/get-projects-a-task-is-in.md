# Get projects a task is in with Asana

Retrieves the projects for a task from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `tasks/:task_gid/projects`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get projects a task is in](https://developers.asana.com/reference/getprojectsfortask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task_gid` | path | `string` | yes |

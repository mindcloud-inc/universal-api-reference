# Get tasks from a project with Asana

Retrieves tasks from a project in Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:project_gid/tasks`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get tasks from a project](https://developers.asana.com/reference/gettasksforproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_gid` | path | `string` | yes | — |
| `opt_fields` | query | `string` | no | Send multiple values as a array. |

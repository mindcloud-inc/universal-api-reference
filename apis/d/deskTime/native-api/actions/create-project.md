# Create Project with DeskTime

Creates a new project in DeskTime with an optional task.

## Endpoint

- **Method:** `POST`
- **Path:** `/create-project`
- **Base URL:** `https://desktime.com/api/v2/json`
- **Official documentation:** [Create Project](https://help.desktime.com/hc/en-us/articles/25495264299293-How-to-create-a-project-with-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | query | `string` | yes | Project name. |
| `task` | query | `string` | no | Task name. |

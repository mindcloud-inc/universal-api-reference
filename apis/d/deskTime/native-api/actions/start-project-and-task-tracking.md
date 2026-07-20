# Start Project and Task Tracking with DeskTime

Starts time tracking for a DeskTime project and task.

## Endpoint

- **Method:** `GET`
- **Path:** `/start-project`
- **Base URL:** `https://desktime.com/api/v2/json`
- **Official documentation:** [Start Project and Task Tracking](https://help.desktime.com/hc/en-us/articles/25495406925853-How-to-start-a-project-and-task-with-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | query | `string` | yes | Project name. |
| `task` | query | `string` | no | Task name. |

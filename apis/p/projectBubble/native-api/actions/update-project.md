# Update Project with Project Bubble

Updates an existing project in Project Bubble.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:project_id`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Update Project](https://help.proprofsproject.com/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The Project Bubble project ID to update. |
| `project_name` | body | `string` | no | The updated project name. |

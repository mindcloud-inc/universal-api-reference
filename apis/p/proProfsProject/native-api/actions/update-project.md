# Update Project with ProProfs Project

Updates an existing project in ProProfs Project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/{{project_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Update Project](https://help.proprofsproject.com/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The updated project description. |
| `project_id` | path | `string` | yes | The project ID to update. |
| `project_name` | body | `string` | no | The updated project name. |

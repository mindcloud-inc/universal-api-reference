# Create Project with ProProfs Project

Creates a new project in ProProfs Project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Create Project](https://help.proprofsproject.com/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The project description. |
| `project_name` | body | `string` | yes | The project name. |

# Create Project with Clientary

Creates a new project in Clientary.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://{subdomain}.clientary.com/api/v2`
- **Official documentation:** [Create Project](https://www.clientary.com/api/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project.budget_type` | body | `string` | no | The project budget type. |
| `project.name` | body | `string` | yes | The project name. |
| `project.number` | body | `string` | no | Optional unique project number. |
| `project.project_type` | body | `string` | no | The project type. |
| `project.rate` | body | `number` | yes | The project hourly rate. |

# Update Project with Clientary

Updates a project in Clientary by project ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:id`
- **Base URL:** `https://{subdomain}.clientary.com/api/v2`
- **Official documentation:** [Update Project](https://www.clientary.com/api/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Clientary project ID. |
| `project.budget_type` | body | `string` | no | The project budget type. |
| `project.name` | body | `string` | no | The project name. |
| `project.number` | body | `string` | no | Optional unique project number. |
| `project.project_type` | body | `string` | no | The project type. |
| `project.rate` | body | `number` | no | The project hourly rate. |

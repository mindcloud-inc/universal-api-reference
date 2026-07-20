# Create Project with Timewax

Creates a new project in Timewax.

## Endpoint

- **Method:** `POST`
- **Path:** `project/add/`
- **Base URL:** `https://api.timewax.com/`
- **Official documentation:** [Create Project](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231599173)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request.project.code` | body | `string` | yes | Code of the project. |
| `request.project.name` | body | `string` | yes | Name of the project. |
| `request.project.company` | body | `string` | yes | Code or name of the client. |
| `request.project.organisationalUnit` | body | `string` | yes | Code or name of the department. |
| `request.project.projectManager` | body | `string` | yes | Code or name of the project manager. |
| `request.project.currency` | body | `string` | yes | Project currency. |

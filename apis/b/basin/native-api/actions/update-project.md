# Update Project with Basin

Updates an existing project in Basin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/projects/:id`
- **Base URL:** `https://usebasin.com`
- **Official documentation:** [Update Project](https://usebasin.com/api_docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the project to update. |
| `project` | body | `object` | no | Project fields to update. |
| `project.name` | body | `string` | no | New project name. |

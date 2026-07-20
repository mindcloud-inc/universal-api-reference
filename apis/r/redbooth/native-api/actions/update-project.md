# Update Project with Redbooth

Updates an existing project in Redbooth.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:id`
- **Base URL:** `https://redbooth.com/api/3`
- **Official documentation:** [Update Project](https://redbooth.com/api/api-docs/#page:projects,header:projects-project-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Redbooth project ID |
| `name` | body | `string` | yes | Updated project name |

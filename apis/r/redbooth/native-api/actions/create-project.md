# Create Project with Redbooth

Creates a new project in Redbooth.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://redbooth.com/api/3`
- **Official documentation:** [Create Project](https://redbooth.com/api/api-docs/#page:projects,header:projects-project-list-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Project name |
| `organization_id` | body | `number` | yes | Redbooth organization ID |

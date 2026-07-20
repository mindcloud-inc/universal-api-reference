# Update Project with Frameshift

Updates an existing project in Frameshift.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/projects/:project_id`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Update Project](https://mosaic.frameshift.io/api/#api-Collections-UpdateProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | Resource identifier for the project to access |
| `name` | body | `string` | no | The name of the project |
| `description` | body | `string` | no | The details surrounding the project |

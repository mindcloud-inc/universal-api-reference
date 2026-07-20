# Update Project with Braintrust

Updates an existing project in Braintrust.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/project/:project_id`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Update Project](https://braintrust.dev/docs/api-reference/projects/partially-update-project.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id. |
| `description` | body | `string` | no | Updated project description. |

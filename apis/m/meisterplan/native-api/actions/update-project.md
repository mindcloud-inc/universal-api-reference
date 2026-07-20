# Update Project with Meisterplan

Updates an existing project in Meisterplan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/scenarios/:scenarioId/projects/:projectId`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Update Project](https://api.us.meisterplan.com/docs/api.html#operation/UpdateProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `projectId` | path | `string` | yes | Internal Meisterplan project identifier. |
| `name` | body | `string` | no | Updated project name. |
| `notes` | body | `string` | no | Updated project notes. |

# Delete Project with Meisterplan

Deletes an existing project from Meisterplan.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/scenarios/:scenarioId/projects/:projectId`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Delete Project](https://api.us.meisterplan.com/docs/api.html#operation/DeleteProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `projectId` | path | `string` | yes | Internal Meisterplan project identifier. |

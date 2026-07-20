# Get Project with Meisterplan

Retrieves a project from Meisterplan.

## Endpoint

- **Method:** `GET`
- **Path:** `/scenarios/:scenarioId/projects/:projectId`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Get Project](https://api.us.meisterplan.com/docs/api.html#operation/GetProjectById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `projectId` | path | `string` | yes | Internal Meisterplan project identifier. |

# Create Project with Meisterplan

Creates a new project in Meisterplan.

## Endpoint

- **Method:** `POST`
- **Path:** `/scenarios/:scenarioId/projects`
- **Base URL:** `https://api.us.meisterplan.com/v1`
- **Official documentation:** [Create Project](https://api.us.meisterplan.com/docs/api.html#operation/CreateProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | Internal Meisterplan scenario identifier. |
| `name` | body | `string` | yes | Project name. |
| `start` | body | `string` | no | Project start date in YYYY-MM-DD format. |
| `finish` | body | `string` | no | Project finish date in YYYY-MM-DD format. |
| `projectKey` | body | `string` | no | Unique Meisterplan project key. |
| `notes` | body | `string` | no | Project notes. |

# Update Project with v0

Updates an existing project in v0.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/projects/:projectId`
- **Base URL:** `https://api.v0.dev`
- **Official documentation:** [Update Project](https://v0.app/docs/api/platform/reference/projects/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The ID of the project to update. |
| `name` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `instructions` | body | `string` | no | — |
| `privacy` | body | `string` | no | — |

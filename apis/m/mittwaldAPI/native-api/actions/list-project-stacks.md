# List Project Stacks with mittwald

Retrieves project stacks from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:projectId/stacks`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List Project Stacks](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the project. |

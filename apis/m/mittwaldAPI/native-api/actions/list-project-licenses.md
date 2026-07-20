# List Project Licenses with mittwald

Retrieves project licenses from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:projectId/licenses`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List Project Licenses](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the project. |

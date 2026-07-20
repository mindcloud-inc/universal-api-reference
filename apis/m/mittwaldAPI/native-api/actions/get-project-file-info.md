# Get Project File Info with mittwald

Retrieves project file information from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:projectId/filesystem-files`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [Get Project File Info](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the project. |

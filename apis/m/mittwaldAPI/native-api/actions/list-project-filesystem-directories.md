# List Project Filesystem Directories with mittwald

Retrieves project filesystem directories from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:projectId/filesystem-directories`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List Project Filesystem Directories](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the project. |

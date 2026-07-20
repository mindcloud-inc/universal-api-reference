# Get Project File Content with mittwald

Retrieves project file content from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:projectId/filesystem-file-content`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [Get Project File Content](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the project. |

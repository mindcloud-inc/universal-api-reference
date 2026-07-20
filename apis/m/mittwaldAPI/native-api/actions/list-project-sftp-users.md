# List Project SFTP Users with mittwald

Retrieves project SFTP users from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:projectId/sftp-users`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List Project SFTP Users](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the project. |

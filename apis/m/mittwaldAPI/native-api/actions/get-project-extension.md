# Get Project Extension with mittwald

Retrieves project extension from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:projectId/extensions/:extensionId`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [Get Project Extension](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extensionId` | path | `string` | yes | Extension ID |
| `projectId` | path | `string` | yes | Project ID |

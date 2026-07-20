# List Project Mail Addresses with mittwald

Retrieves project mail addresses from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:projectId/mail-addresses`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List Project Mail Addresses](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the project. |

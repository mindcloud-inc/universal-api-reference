# Get Project Version Upload URL with Openlayer

Retrieves a version upload URL for a project in Openlayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/versions/presigned-url`
- **Base URL:** `https://api.openlayer.com/v1`
- **Official documentation:** [Get Project Version Upload URL](https://api.openlayer.com/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectName` | query | `string` | yes | Artifact object name. |
| `projectId` | path | `string` | yes | The Openlayer project ID. |
| `storageInterface` | query | `string` | yes | Storage platform for the upload URL. |

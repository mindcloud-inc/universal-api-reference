# Get Schema Version with Google Cloud Document AI

Retrieves a schema version from Google Cloud Document AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/schemas/:schemasId/schemaVersions/:schemaVersionsId`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Get Schema Version](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas.schemaVersions/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schemasId` | path | `string` | no | Document schema ID. |
| `schemaVersionsId` | path | `string` | no | Document schema version ID. |

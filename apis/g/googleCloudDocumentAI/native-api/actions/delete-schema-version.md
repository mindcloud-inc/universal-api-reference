# Delete Schema Version with Google Cloud Document AI

Deletes a schema version from Google Cloud Document AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/schemas/:schemasId/schemaVersions/:schemaVersionsId`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Delete Schema Version](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas.schemaVersions/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schemasId` | path | `string` | no | Document schema ID. |
| `schemaVersionsId` | path | `string` | no | Document schema version ID. |

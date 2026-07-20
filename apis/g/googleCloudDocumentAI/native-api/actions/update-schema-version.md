# Update Schema Version with Google Cloud Document AI

Updates an existing schema version in Google Cloud Document AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/schemas/:schemasId/schemaVersions/:schemaVersionsId`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Update Schema Version](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas.schemaVersions/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schemasId` | path | `string` | no | Document schema ID. |
| `schemaVersionsId` | path | `string` | no | Document schema version ID. |

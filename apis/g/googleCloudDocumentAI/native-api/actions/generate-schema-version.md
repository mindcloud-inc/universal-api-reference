# Generate Schema Version with Google Cloud Document AI

Generates a schema version in Google Cloud Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/schemas/:schemasId/schemaVersions:generate`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Generate Schema Version](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas.schemaVersions/generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schemasId` | path | `string` | no | Document schema ID. |

# List Schema Versions with Google Cloud Document AI

Finds schema versions in Google Cloud Document AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/schemas/:schemasId/schemaVersions`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [List Schema Versions](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas.schemaVersions/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schemasId` | path | `string` | no | Document schema ID. |

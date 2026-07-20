# Update Schema with Google Cloud Document AI

Updates an existing schema in Google Cloud Document AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/schemas/:schemasId`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Update Schema](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schemasId` | path | `string` | no | Document schema ID. |
| `displayName` | body | `string` | no | Schema display name. |
| `labels` | body | `object` | no | Schema labels. |

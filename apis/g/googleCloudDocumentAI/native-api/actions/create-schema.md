# Create Schema with Google Cloud Document AI

Creates a new schema in Google Cloud Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/schemas`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Create Schema](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.schemas/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `displayName` | body | `string` | yes | Schema display name. |
| `labels` | body | `object` | no | Schema labels. |

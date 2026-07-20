# Create Processor with Google Cloud Document AI

Creates a new processor in Google Cloud Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/processors`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Create Processor](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Processor type, such as OCR_PROCESSOR. |
| `displayName` | body | `string` | yes | Human-readable processor display name. |
| `kmsKeyName` | body | `string` | no | Optional Cloud KMS key name for encryption. |

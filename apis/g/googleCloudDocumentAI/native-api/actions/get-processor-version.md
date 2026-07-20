# Get Processor Version with Google Cloud Document AI

Retrieves a processor version from Google Cloud Document AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Get Processor Version](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processorsId` | path | `string` | no | Document AI processor ID. |
| `processorVersionsId` | path | `string` | no | Processor version ID. |

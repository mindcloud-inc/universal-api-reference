# Get Processor Version Evaluation with Google Cloud Document AI

Retrieves a processor version evaluation from Google Cloud Document AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId/evaluations/:evaluationsId`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Get Processor Version Evaluation](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions.evaluations/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `evaluationsId` | path | `string` | no | Processor version evaluation ID. |
| `processorsId` | path | `string` | no | Document AI processor ID. |
| `processorVersionsId` | path | `string` | no | Processor version ID. |

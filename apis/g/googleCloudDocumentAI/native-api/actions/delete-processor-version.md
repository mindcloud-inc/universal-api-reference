# Delete Processor Version with Google Cloud Document AI

Deletes a processor version from Google Cloud Document AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Delete Processor Version](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processorsId` | path | `string` | no | Document AI processor ID. |
| `processorVersionsId` | path | `string` | no | Processor version ID. |

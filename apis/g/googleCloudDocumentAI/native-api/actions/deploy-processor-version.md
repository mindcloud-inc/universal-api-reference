# Deploy Processor Version with Google Cloud Document AI

Deploys a processor version in Google Cloud Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId:deploy`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Deploy Processor Version](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions/deploy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processorsId` | path | `string` | no | Document AI processor ID. |
| `processorVersionsId` | path | `string` | no | Processor version ID. |

# List Processor Version Evaluations with Google Cloud Document AI

Finds processor version evaluations in Google Cloud Document AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId/evaluations`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [List Processor Version Evaluations](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions.evaluations/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processorsId` | path | `string` | no | Document AI processor ID. |
| `processorVersionsId` | path | `string` | no | Processor version ID. |

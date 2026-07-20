# Evaluate Processor Version with Google Cloud Document AI

Evaluates a processor version in Google Cloud Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions/:processorVersionsId:evaluateProcessorVersion`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Evaluate Processor Version](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions/evaluateProcessorVersion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processorsId` | path | `string` | yes | Document AI processor ID. |
| `processorVersionsId` | path | `string` | yes | Processor version ID. |
| `evaluationDocuments` | body | `object` | yes | Documents used to evaluate the processor version. |

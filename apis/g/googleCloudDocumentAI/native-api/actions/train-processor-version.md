# Train Processor Version with Google Cloud Document AI

Trains a processor version in Google Cloud Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/processors/:processorsId/processorVersions:train`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Train Processor Version](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors.processorVersions/train)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processorsId` | path | `string` | yes | Document AI processor ID. |
| `processorVersion` | body | `object` | yes | Processor version configuration to train. |
| `documentSchema` | body | `object` | no | Document schema used for training. |
| `inputData` | body | `object` | yes | Training input data configuration. |

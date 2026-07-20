# Batch Process Documents With Processor with Google Cloud Document AI

Batch processes documents with a Google Cloud Document AI processor.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:projectsId/locations/:locationsId/processors/:processorsId:batchProcess`
- **Base URL:** `https://documentai.googleapis.com`
- **Official documentation:** [Batch Process Documents With Processor](https://cloud.google.com/document-ai/docs/reference/rest/v1/projects.locations.processors/batchProcess)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processorsId` | path | `string` | yes | Document AI processor ID. |
| `inputDocuments` | body | `object` | yes | Batch input document source configuration. |
| `documentOutputConfig` | body | `object` | yes | Output destination for batch processing results. |
| `skipHumanReview` | body | `boolean` | no | Whether to skip human review. |
| `processOptions` | body | `object` | no | Optional processing configuration. |
| `labels` | body | `object` | no | Request labels to attach to processing metadata. |

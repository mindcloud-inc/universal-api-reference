# Get Classification Batch Results with Extracta.ai

Retrieves classification batch results from Extracta.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/documentClassification/getResults`
- **Base URL:** `https://api.extracta.ai/api/v1`
- **Official documentation:** [Get Classification Batch Results](https://docs.extracta.ai/document-classification-api/api-endpoints-document-classification/6.-get-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classificationId` | body | `string` | yes | Unique identifier for the classification. |
| `batchId` | body | `string` | yes | Unique identifier for the batch. |

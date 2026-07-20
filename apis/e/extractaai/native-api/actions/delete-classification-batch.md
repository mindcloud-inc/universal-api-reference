# Delete Classification Batch with Extracta.ai

Deletes a classification batch from Extracta.ai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/documentClassification/deleteBatch`
- **Base URL:** `https://api.extracta.ai/api/v1`
- **Official documentation:** [Delete Classification Batch](https://docs.extracta.ai/document-classification-api/api-endpoints-document-classification/4.-delete-data/4.2-delete-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classificationId` | body | `string` | yes | Unique identifier for the classification. |
| `batchId` | body | `string` | yes | Unique identifier for the batch. |

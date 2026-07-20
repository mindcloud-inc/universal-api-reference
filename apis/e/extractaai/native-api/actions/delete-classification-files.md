# Delete Classification Files with Extracta.ai

Deletes classification files from Extracta.ai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/documentClassification/deleteFiles`
- **Base URL:** `https://api.extracta.ai/api/v1`
- **Official documentation:** [Delete Classification Files](https://docs.extracta.ai/document-classification-api/api-endpoints-document-classification/4.-delete-data/4.3-delete-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classificationId` | body | `string` | yes | Unique identifier for the classification. |
| `batchId` | body | `string` | yes | Unique identifier for the batch. |
| `fileIds[]` | body | `array<string>` | yes | List of file identifiers to delete. |

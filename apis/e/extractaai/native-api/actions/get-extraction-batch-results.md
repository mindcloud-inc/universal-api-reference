# Get Extraction Batch Results with Extracta.ai

Retrieves extraction batch results from Extracta.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/getBatchResults`
- **Base URL:** `https://api.extracta.ai/api/v1`
- **Official documentation:** [Get Extraction Batch Results](https://docs.extracta.ai/data-extraction-api/api-endpoints-data-extraction/6.-get-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extractionId` | body | `string` | yes | Unique identifier for the extraction. |
| `batchId` | body | `string` | yes | Unique identifier for the batch. |

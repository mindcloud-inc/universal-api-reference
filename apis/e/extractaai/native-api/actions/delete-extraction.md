# Delete Extraction with Extracta.ai

Deletes an existing extraction from Extracta.ai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/deleteExtraction`
- **Base URL:** `https://api.extracta.ai/api/v1`
- **Official documentation:** [Delete Extraction](https://docs.extracta.ai/data-extraction-api/api-endpoints-data-extraction/4.-delete-extraction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extractionId` | body | `string` | yes | Unique identifier for the extraction. |
| `batchId` | body | `string` | no | Unique identifier for the batch. |
| `fileId` | body | `string` | no | Unique identifier for the file. |

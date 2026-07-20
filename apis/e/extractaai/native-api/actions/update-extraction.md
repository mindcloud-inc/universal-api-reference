# Update Extraction with Extracta.ai

Updates an existing extraction in Extracta.ai.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/updateExtraction`
- **Base URL:** `https://api.extracta.ai/api/v1`
- **Official documentation:** [Update Extraction](https://docs.extracta.ai/data-extraction-api/api-endpoints-data-extraction/3.-update-extraction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extractionId` | body | `string` | yes | Unique identifier for the extraction. |
| `extractionDetails` | body | `object` | yes | Object containing the extraction fields to update. |

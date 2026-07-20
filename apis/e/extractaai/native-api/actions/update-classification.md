# Update Classification with Extracta.ai

Updates an existing classification in Extracta.ai.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/documentClassification/updateClassification`
- **Base URL:** `https://api.extracta.ai/api/v1`
- **Official documentation:** [Update Classification](https://docs.extracta.ai/document-classification-api/api-endpoints-document-classification/3.-update-classification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classificationId` | body | `string` | yes | Unique identifier for the classification. |
| `classificationDetails` | body | `object` | yes | Object containing the classification fields to update. |

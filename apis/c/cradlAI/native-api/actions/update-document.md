# Update Document with Cradl AI

Updates an existing document in Cradl AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/documents/:documentId`
- **Base URL:** `https://api.cradl.ai/v1`
- **Official documentation:** [Update Document](https://docs.cradl.ai/api-reference/patch-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Identifier of the document to update. |
| `name` | body | `string` | no | Updated document name. |
| `description` | body | `string` | no | Updated document description. |
| `datasetId` | body | `string` | no | Updated dataset identifier. |
| `groundTruth[]` | body | `array<object>` | no | Updated ground truth labels for the document. |
| `metadata` | body | `object` | no | Updated metadata attached to the document. |
| `retentionInDays` | body | `number` | no | Updated retention period in days. |

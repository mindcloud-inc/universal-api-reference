# Request Document Export with Smartcat

Creates a document export task in Smartcat.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/integration/v1/document/export`
- **Base URL:** `https://smartcat.ai`
- **Official documentation:** [Request Document Export](https://developers.smartcat.com/api/#request-the-documents-export)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds` | query | `string` | yes | One or more document IDs in documentId_targetLanguageId format Send multiple values as a string separated by `,`. |
| `type` | query | `string` | no | Export type, such as target |
| `stageNumber` | query | `number` | no | Workflow stage number to export from |

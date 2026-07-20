# Delete Document with Nanonets OCR

## Endpoint

- **Method:** `DELETE`
- **Path:** `/workflows/:workflow_id/documents/:document_id`
- **Base URL:** `https://app.nanonets.com/api/v4`
- **Official documentation:** [Delete Document](https://apidocs.nanonets.com/docs/api/document-processing/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `list` | yes | Workflow ID that owns the document. |
| `document_id` | path | `string` | yes | Document ID to delete. |

# Download File with Koncile OCR

## Endpoint

- **Method:** `GET`
- **Path:** `/fetch_file`
- **Base URL:** `https://api.koncile.ai/v1`
- **Official documentation:** [Download File](https://docs.koncile.ai/api-setup/documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | query | `number` | no | Download the original file for this document ID. |
| `task_id` | query | `string` | no | Download the original file by task ID when document_id is not provided. |

# Download Files Batch with Koncile OCR

## Endpoint

- **Method:** `POST`
- **Path:** `/fetch_files_batch`
- **Base URL:** `https://api.koncile.ai/v1`
- **Official documentation:** [Download Files Batch](https://docs.koncile.ai/api-setup/documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_ids[]` | body | `array<number>` | no | A list of document IDs to download as a ZIP archive. Send multiple values as a array. |
| `task_ids[]` | body | `array<string>` | no | A list of task IDs to resolve and download as a ZIP archive. Send multiple values as a array. |

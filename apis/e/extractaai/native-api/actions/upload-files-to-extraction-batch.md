# Upload Files to Extraction Batch with Extracta.ai

Uploads files to an extraction batch in Extracta.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploadFiles`
- **Base URL:** `https://api.extracta.ai/api/v1`
- **Official documentation:** [Upload Files to Extraction Batch](https://docs.extracta.ai/data-extraction-api/api-endpoints-data-extraction/5.-upload-files)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extractionId` | body | `string` | yes | Unique identifier for the extraction. |
| `batchId` | body | `string` | yes | Unique identifier for the batch. |
| `files` | body | `file` | yes | One or more files to upload. Send multiple values as a array. |

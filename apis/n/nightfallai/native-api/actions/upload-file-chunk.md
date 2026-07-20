# Upload File Chunk with Nightfall.ai

Uploads a file chunk to Nightfall.ai.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v3/upload/:fileId`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Upload File Chunk](https://help.nightfall.ai/developer-api/key-concepts/file_scan/scan_api_calls)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | The upload UUID returned when the file upload was created. |
| `uploadOffset` | query | `number` | yes | Zero-based byte offset where this chunk should be written. |
| `chunk` | body | `file` | yes | Binary file chunk to upload. |

# Create File Upload with Nightfall.ai

Creates a file upload in Nightfall.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/upload`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Create File Upload](https://help.nightfall.ai/developer-api/key-concepts/file_scan/scan_api_calls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileSizeBytes` | body | `number` | yes | Total size of the file in bytes. |
| `mimeType` | body | `string` | no | Optional MIME type for the file upload. |

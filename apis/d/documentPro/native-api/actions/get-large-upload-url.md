# Get Large Upload URL with DocumentPro

Retrieves a large-file upload URL from DocumentPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/documents/upload_url`
- **Base URL:** `https://api.documentpro.ai`
- **Official documentation:** [Get Large Upload URL](https://docs.documentpro.ai/docs/using-api/extract/upload-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | query | `string` | yes | The original file name for the large upload. |

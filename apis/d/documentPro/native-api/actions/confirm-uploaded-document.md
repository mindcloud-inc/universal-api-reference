# Confirm Uploaded Document with DocumentPro

Confirms a large uploaded document in DocumentPro.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/documents`
- **Base URL:** `https://api.documentpro.ai`
- **Official documentation:** [Confirm Uploaded Document](https://docs.documentpro.ai/docs/using-api/extract/upload-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_extension` | body | `string` | yes | The uploaded file extension, for example pdf. |
| `file_name` | body | `string` | yes | The original file name for the uploaded file. |
| `upload_url` | body | `string` | yes | The temporary upload URL returned by Get Large Upload URL. |

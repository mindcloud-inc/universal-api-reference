# Initialize File Upload with Grok

Creates a chunked file upload session in Grok.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/files:initialize`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Initialize File Upload](https://docs.x.ai/developers/rest-api-reference/files/upload#initialize-a-file-upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | File name to initialize. |
| `content_type` | body | `string` | yes | MIME content type for the file. |

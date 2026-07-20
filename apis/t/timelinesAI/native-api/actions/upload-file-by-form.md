# Upload File by Form with TimelinesAI

Creates a TimelinesAI file from multipart form data.

## Endpoint

- **Method:** `POST`
- **Path:** `/files_upload`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [Upload File by Form](https://timelinesai.mintlify.app/public-api-reference/upload-a-file-in-x-form-encoded-http-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | File to upload. |
| `filename` | body | `string` | no | Optional filename to store for the uploaded file. |
| `content_type` | body | `string` | no | Optional MIME type for the uploaded file. |

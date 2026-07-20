# Upload File by URL with TimelinesAI

Creates a TimelinesAI file from a public URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/files`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [Upload File by URL](https://timelinesai.mintlify.app/public-api-reference/upload-a-file-using-a-publicly-accessible-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `download_url` | body | `string` | yes | Publicly accessible URL of the file to upload. |
| `filename` | body | `string` | no | Optional filename to store for the uploaded file. |
| `content_type` | body | `string` | no | Optional MIME type for the uploaded file. |

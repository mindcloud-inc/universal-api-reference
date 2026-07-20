# Get File Upload URL with Needle

Retrieves a signed file upload URL from Needle.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/files/upload_url`
- **Base URL:** `https://needle.app`
- **Official documentation:** [Get File Upload URL](https://docs.needle.app/docs/api-reference/get-upload-url/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content_type` | query | `string` | yes | MIME type to generate an upload URL for |

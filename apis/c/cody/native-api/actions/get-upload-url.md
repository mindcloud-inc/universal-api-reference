# Get Upload URL with Cody

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads/signed-url`
- **Base URL:** `https://getcody.ai/api/v1`
- **Official documentation:** [Get Upload URL](https://developers.meetcody.ai/operation/operation-get-uploads-signed-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | body | `string` | no | Original file name to upload, including the file extension. |
| `content_type` | body | `string` | no | MIME content type of the file. |

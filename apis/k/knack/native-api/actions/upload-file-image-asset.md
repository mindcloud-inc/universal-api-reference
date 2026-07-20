# Upload File Image Asset with Knack

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/{applicationId}/assets/:asset_type/upload`
- **Base URL:** `https://api.knack.com/v1`
- **Official documentation:** [Upload File Image Asset](https://docs.knack.com/reference/fileimage-uploads)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset_type` | path | `string` | yes | Upload target type: file or image. |
| `files` | body | `file` | yes | Remote URL, base64, or binary content for the file or image to upload. |

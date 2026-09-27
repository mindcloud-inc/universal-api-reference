# Complete multipart video upload with ConnectSafely

Call after all video chunks have been PUT to the pre-signed URLs. Only needed for MULTIPART uploads (large videos).

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/upload/complete`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Complete multipart video upload](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-upload-complete-upload-complete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no |  |
| `mediaArtifactUrn` | body | `string` | yes | From /upload/init response. |
| `multipartMetadata` | body | `string` | no | From /upload/init response. |
| `partUploadResponses` | body | `array` | yes |  |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |

## Error status codes

`401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.

# Upload message attachment with ConnectSafely

Upload a file to attach to a LinkedIn message (used with POST /conversations/send). **Send the file as the RAW binary request body — do NOT use multipart/form-data.** Set the request `Content-Type` header to the file's actual MIME type, and pass `accountId` and `filename` in the query string. **To make an image render inline as a photo in the conversation, the `Content-Type` MUST be an image type** (`image/png`, `image/jpeg`, `image/gif`, `image/webp`) — this uploads it as a LinkedIn photo asset. Any other content type is stored as a downloadable file attachment. The response's `attachment` object must then be passed to POST /conversations/send wrapped in a `file` key: `{ "attachments": [{ "file": <attachment> }] }`. Example: `curl -X POST "https://api.connectsafely.ai/linkedin/conversations/upload-attachment?accountId=acc_123&filename=photo.png" -H "Authorization: Bearer <api_key>" -H "Content-Type: image/png" --data-binary @photo.png`

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/upload-attachment`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Upload message attachment](https://connectsafely.ai/docs/api/linkedin-messaging/post-conversations-upload-attachment-conversations-upload-attachment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | LinkedIn account ID. If omitted, resolved from the authenticated user's default account. |
| `filename` | query | `string` | no | Original file name including extension (e.g. "photo.png"). Defaults to "attachment" if omitted. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `attachment` | `object` | Pass this back to POST /conversations/send as { attachments: [{ file: <this> }] }. |
| `attachment.assetUrn` | `string` |  |
| `attachment.byteSize` | `number` |  |
| `attachment.mediaType` | `string` |  |
| `attachment.name` | `string` |  |

## Error status codes

`400`, `401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.

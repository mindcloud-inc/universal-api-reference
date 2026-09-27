# Check document (PDF) processing status with ConnectSafely

After PUTting a document to the pre-signed URL from /posts/upload/init, poll this until status is READY. LinkedIn rasterizes each page into preview images first; the document cannot be posted until it is READY. Only needed for mediaType=document.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/upload/document-status`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Check document (PDF) processing status](https://connectsafely.ai/docs/api/linkedin-posts/get-posts-upload-document-status-upload-document-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assetUrn` | query | `string` | yes | Document asset URN from /posts/upload/init. |
| `accountId` | query | `string` | no | LinkedIn account ID. If omitted, uses the default account. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `status` | `list` |  |
| `ready` | `boolean` | true when status is READY (safe to call /posts/create). |

## Error status codes

`401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.

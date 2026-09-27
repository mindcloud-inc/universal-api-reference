# Upload media and create a LinkedIn post (server-side) with ConnectSafely

Downloads a file from the provided URL, uploads it to LinkedIn server-side, and creates a post. This is a single-step alternative to the multi-step upload/init + upload + create flow. Maximum file size is 100MB. Designed for MCP and API clients that cannot perform direct pre-signed URL uploads.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/upload-and-post`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Upload media and create a LinkedIn post (server-side)](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-upload-and-post-upload-and-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID. If omitted, uses the default account. |
| `fileUrl` | body | `string` | yes | Public URL of the file to download and upload to LinkedIn. Maximum 100MB. |
| `text` | body | `string` | yes | Post text content. |
| `mediaType` | body | `list` | yes | Type of media being uploaded. Accepted values: `image`, `video`. |
| `visibility` | body | `list` | no | Post visibility. Accepted values: `ANYONE`, `CONNECTIONS_ONLY`. Default: `ANYONE`. |
| `altText` | body | `string` | no | Alt text for images. Default: ``. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `postUrn` | `string` | URN of the created post. |
| `shareUrn` | `string` | Share URN of the created post. |
| `accountId` | `string` | LinkedIn account ID used. |

### Example response

```json
{
  "success": true,
  "postUrn": "urn:li:share:7123456789",
  "shareUrn": "urn:li:share:7123456789",
  "accountId": "696ce9e780e0483585e4e553"
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.

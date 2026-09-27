# Initialize media upload — get pre-signed URL(s) with ConnectSafely

Returns pre-signed URL(s) from LinkedIn for direct client upload. For images, documents, and small videos: returns a single uploadUrl. For large videos: returns partUploadRequests (4MB chunks). The API never touches media bytes — the client uploads directly to LinkedIn. **Documents (PDF):** after PUTting the bytes, poll GET /posts/upload/document-status until ready before calling /posts/create. **Company page:** to author the post as a company page you administer, pass companyUrn here so the asset is registered to the organization — required, otherwise the company-authored post silently fails to publish.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/upload/init`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Initialize media upload — get pre-signed URL(s)](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-upload-init-upload-init)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID. |
| `mediaType` | body | `list` | yes | image / video / document (PDF). Documents upload as SINGLE and require a processing poll (see /posts/upload/document-status). Accepted values: `image`, `video`, `document`. |
| `fileSize` | body | `number` | yes | File size in bytes. |
| `filename` | body | `string` | yes | Filename with extension. |
| `companyUrn` | body | `string` | no | Optional. When the post will be authored by a company page you administer, pass the company URN here so the uploaded asset is registered with the organization as owner. Required for company-page image/video posts — without it LinkedIn accepts the later share (HTTP 200) but silently creates no post (no share URN). Must match the companyUrn passed to /posts/create. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `uploadType` | `list` |  |
| `assetUrn` | `string` | Pass this to /posts/create. |
| `recipes` | `array` |  |
| `uploadUrl` | `string` | Pre-signed URL for SINGLE uploads. |
| `uploadHeaders` | `object` | Headers to include in the PUT request. |
| `mediaArtifactUrn` | `string` | For MULTIPART — pass to /upload/complete. |
| `partUploadRequests` | `array` | For MULTIPART — chunk upload URLs. |
| `multipartMetadata` | `string` | For MULTIPART — pass to /upload/complete. |

## Error status codes

`401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.

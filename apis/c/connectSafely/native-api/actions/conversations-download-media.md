# Download media from message with ConnectSafely

Download media (images, files, videos, audio) from a LinkedIn messaging URL. Uses account session cookies for authentication. No proxy is used — media is fetched directly from LinkedIn CDN. Supports URLs from www.linkedin.com/dms/prv/ (private messaging media) and media.licdn.com (CDN-hosted media).

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/download-media`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Download media from message](https://connectsafely.ai/docs/api/linkedin-messaging/post-conversations-download-media-conversations-download-media)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | yes | LinkedIn account ID |
| `url` | body | `string` | yes | Media URL from message attachment (www.linkedin.com or media.licdn.com) |

## Error status codes

`400`, `401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.

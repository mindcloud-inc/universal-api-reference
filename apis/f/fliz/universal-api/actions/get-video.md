# Fliz: Get video

Retrieves a video from your Fliz account.

```
GET https://connect.mindcloud.co/v1/universal/fliz/latest/actions/get-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fliz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fliz/latest/actions/get-video?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fliz/latest/actions/get-video?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The UUID of the video to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "error": {},
      "format": "string",
      "id": "string",
      "lang": "string",
      "music": {},
      "remotionConfiguration": {},
      "step": "string",
      "title": "string",
      "url": "https://example.com",
      "voiceId": "string",
      "watermark": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Video category. |
| `createdAt` | date | Creation timestamp. |
| `error` | object | Provider error payload when generation fails. |
| `format` | string | Video output format. |
| `id` | string | Video UUID. |
| `lang` | string | Video language code. |
| `music` | object | Music file metadata when present. |
| `remotionConfiguration` | object | Rendering configuration. |
| `step` | string | Current processing step. |
| `title` | string | Video title. |
| `url` | string | Rendered video URL when available. |
| `voiceId` | string | Voice ID used by the video. |
| `watermark` | object | Watermark metadata when present. |

## Native endpoint

Through the native Fliz API, this operation is `GET /api/rest/videos/:id` (base URL `https://app.fliz.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video.md) for the provider-specific parameters and requirements.


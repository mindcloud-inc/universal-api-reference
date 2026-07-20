# Freepik: Get Video

Retrieves detailed video information from Freepik.

```
GET https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-video?connectionId=$CONNECTION_ID&id=208014" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "208014"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-video?${params}`, {
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
| `id` | number | yes | Freepik video identifier. Default: `208014`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "created": "2026-05-07T12:00:00.000Z",
      "duration": "string",
      "fps": "string",
      "id": 1,
      "name": "Ava Chen",
      "options": [
        {}
      ],
      "premium": true,
      "previews": [
        {}
      ],
      "quality": "string",
      "tags": [
        {}
      ],
      "thumbnails": [
        {}
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object | Author details. |
| `created` | date | Creation timestamp. |
| `duration` | string | Video duration. |
| `fps` | string | Frames per second. |
| `id` | number | Video ID. |
| `name` | string | Video name. |
| `options` | array<object> | Available video options. |
| `premium` | boolean | Whether the video is premium. |
| `previews` | array<object> | Preview videos. |
| `quality` | string | Video quality. |
| `tags` | array<object> | Tags. |
| `thumbnails` | array<object> | Thumbnail images. |
| `url` | string | Video page URL. |

## Native endpoint

Through the native Freepik API, this operation is `GET /v1/videos/{{id}}` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video.md) for the provider-specific parameters and requirements.


# Pexels: Get Video

Retrieves a video from Pexels by ID.

```
GET https://connect.mindcloud.co/v1/universal/pexels/latest/actions/get-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pexels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pexels/latest/actions/get-video?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pexels/latest/actions/get-video?${params}`, {
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
| `id` | number | yes | Numeric Pexels video ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avg_color": "string",
      "duration": 1,
      "full_res": "string",
      "height": 1,
      "id": 1,
      "image": "string",
      "tags": [
        "string"
      ],
      "url": "https://example.com",
      "user": {},
      "video_files": [
        {}
      ],
      "video_pictures": [
        {}
      ],
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avg_color` | string | Average color when provided by Pexels. |
| `duration` | number | Video duration in seconds. |
| `full_res` | string | Full-resolution video URL when provided by Pexels. |
| `height` | number | Video height in pixels. |
| `id` | number | Pexels video ID. |
| `image` | string | Video preview image URL. |
| `tags` | array<string> | Tags returned by Pexels for the video. |
| `url` | string | Pexels URL for the video. |
| `user` | object | Videographer information. |
| `video_files` | array<object> | Available video file versions. |
| `video_pictures` | array<object> | Preview images for the video. |
| `width` | number | Video width in pixels. |

## Native endpoint

Through the native Pexels API, this operation is `GET /v1/videos/videos/:id` (base URL `https://api.pexels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video.md) for the provider-specific parameters and requirements.


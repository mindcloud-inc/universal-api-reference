# Freepik: Search Videos

Finds Freepik videos by search term and filters.

```
GET https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-videos?connectionId=$CONNECTION_ID&term=car" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "term": "car"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-videos?${params}`, {
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
| `term` | string | yes | Video search term. Freepik returns a validation error when omitted. Default: `car`. |
| `page` | number | no | One-based videos page to request. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "aspect_ratio": "string",
      "author": {},
      "created": "2026-05-07T12:00:00.000Z",
      "duration": "string",
      "id": 1,
      "name": "Ava Chen",
      "premium": true,
      "previews": [
        {}
      ],
      "quality": "string",
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
| `active` | boolean | Whether the video is active. |
| `aspect_ratio` | string | Aspect ratio. |
| `author` | object | Author details. |
| `created` | date | Creation timestamp. |
| `duration` | string | Video duration. |
| `id` | number | Video ID. |
| `name` | string | Video name. |
| `premium` | boolean | Whether the video is premium. |
| `previews` | array<object> | Preview videos. |
| `quality` | string | Video quality. |
| `thumbnails` | array<object> | Thumbnail images. |
| `url` | string | Video page URL. |

## Native endpoint

Through the native Freepik API, this operation is `GET /v1/videos` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-videos.md) for the provider-specific parameters and requirements.


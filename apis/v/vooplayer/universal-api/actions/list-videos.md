# Vooplayer: List Videos

Retrieves videos from Vooplayer by video or project.

```
GET https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/list-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vooplayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/list-videos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/list-videos?${params}`, {
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
| `videoId` | number | no | ID of a video. |
| `videoGroup` | number | no | ID of a project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "videos": {
        "current_page": 1,
        "data": [
          {
            "altID": "string",
            "created": "string",
            "downloadURL": "https://example.com",
            "duration": 1,
            "id": 1,
            "name": "Ava Chen",
            "optimizedUrls": "https://example.com",
            "originalFileURL": "https://example.com",
            "playerSettings": "string",
            "thumbnail": "string",
            "updated": "string",
            "url": "https://example.com",
            "videoGroup": "string"
          }
        ],
        "from": 1,
        "last_page": 1,
        "next_page_url": "https://example.com",
        "per_page": 1,
        "prev_page_url": "https://example.com",
        "to": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `videos.current_page` | number | Current page number. |
| `videos.data` | array<object> | Video rows. |
| `videos.data[].altID` | string | Alternative provider ID. |
| `videos.data[].created` | string | Creation timestamp. |
| `videos.data[].downloadURL` | string | Download URL when available. |
| `videos.data[].duration` | number | Video duration in seconds. |
| `videos.data[].id` | number | Video ID. |
| `videos.data[].name` | string | Video name. |
| `videos.data[].optimizedUrls` | string | Optimized source URLs. |
| `videos.data[].originalFileURL` | string | Original uploaded file URL. |
| `videos.data[].playerSettings` | string | Serialized player settings JSON. |
| `videos.data[].thumbnail` | string | Thumbnail URL. |
| `videos.data[].updated` | string | Last updated timestamp. |
| `videos.data[].url` | string | Current video source URL. |
| `videos.data[].videoGroup` | string | Owning project ID. |
| `videos.from` | number | First row position in this page when available. |
| `videos.last_page` | number | Last page number. |
| `videos.next_page_url` | string | Next page URL when available. |
| `videos.per_page` | number | Page size. |
| `videos.prev_page_url` | string | Previous page URL when available. |
| `videos.to` | number | Last row position in this page when available. |
| `videos.total` | number | Total videos matched. |

## Native endpoint

Through the native Vooplayer API, this operation is `GET /api/videos` (base URL `https://api.spotlightr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-videos.md) for the provider-specific parameters and requirements.


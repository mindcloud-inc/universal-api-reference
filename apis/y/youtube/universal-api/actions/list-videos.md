# YouTube: List Videos

Retrieves one or more videos from YouTube.

```
GET https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-videos?connectionId=$CONNECTION_ID&limit=25&offset=0&part=snippet%2CcontentDetails%2Cstatistics" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "part": "snippet,contentDetails,statistics"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-videos?${params}`, {
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
| `part` | string | yes | Required response parts. Default: `snippet,contentDetails,statistics`. |
| `chart` | string | no | Video chart to retrieve, for example mostPopular. Do not combine with Video ID or My Rating. |
| `id` | string | no | Comma-separated video IDs. Accepts multiple values in one string, delimited by `,`. |
| `myRating` | string | no | Filter by your rating (like/dislike). |
| `regionCode` | string | no | ISO 3166-1 alpha-2 region code. Use with Chart requests such as mostPopular. |
| `videoCategoryId` | string | no | Filter by video category ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentDetails": {
        "duration": "string"
      },
      "etag": "string",
      "id": "string",
      "kind": "string",
      "snippet": {
        "channelTitle": "string",
        "description": "string",
        "publishedAt": "2026-05-07T12:00:00.000Z",
        "title": "string"
      },
      "statistics": {
        "likeCount": "string",
        "viewCount": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentDetails.duration` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `snippet.channelTitle` | string |  |
| `snippet.description` | string |  |
| `snippet.publishedAt` | date |  |
| `snippet.title` | string |  |
| `statistics.likeCount` | string |  |
| `statistics.viewCount` | string |  |

## Native endpoint

Through the native YouTube API, this operation is `GET /youtube/v3/videos` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-videos.md) for the provider-specific parameters and requirements.


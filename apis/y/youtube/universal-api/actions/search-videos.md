# YouTube: Search Videos

Searches YouTube for videos by default.

```
GET https://connect.mindcloud.co/v1/universal/youtube/latest/actions/search-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/search-videos?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youtube/latest/actions/search-videos?${params}`, {
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
| `q` | string | no | Search query term. Default: `mindcloud`. |
| `type` | string | no | Resource type filter (video, channel, playlist). Default: `video`. |
| `channelId` | string | no | Restrict search to a channel ID. |
| `order` | list<string> | no | Sort order for search results. One of: `date`, `rating`, `relevance`, `searchSortUnspecified`, `title`, `videoCount`, `viewCount`. Default: `relevance`. |
| `publishedAfter` | date | no | RFC 3339 timestamp lower bound. |
| `publishedBefore` | date | no | RFC 3339 timestamp upper bound. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": {
        "channelId": "string",
        "kind": "string",
        "playlistId": "string",
        "videoId": "string"
      },
      "snippet": {
        "channelTitle": "string",
        "description": "string",
        "publishedAt": "2026-05-07T12:00:00.000Z",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id.channelId` | string |  |
| `id.kind` | string |  |
| `id.playlistId` | string |  |
| `id.videoId` | string |  |
| `snippet.channelTitle` | string |  |
| `snippet.description` | string |  |
| `snippet.publishedAt` | date |  |
| `snippet.title` | string |  |

## Native endpoint

Through the native YouTube API, this operation is `GET /youtube/v3/search` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-videos.md) for the provider-specific parameters and requirements.


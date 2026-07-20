# YouTube: List Channels

Retrieves one or more channels from YouTube.

```
GET https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-channels?connectionId=$CONNECTION_ID&limit=25&offset=0&part=snippet%2CcontentDetails%2Cstatistics" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "part": "snippet,contentDetails,statistics"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-channels?${params}`, {
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
| `part` | string | yes | Comma-separated list of one or more channel resource properties. Default: `snippet,contentDetails,statistics`. |
| `id` | string | no | Comma-separated YouTube channel IDs. Accepts multiple values in one string, delimited by `,`. |
| `mine` | boolean | no | Return channels owned by the authenticated user. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentDetails": {
        "relatedPlaylists": {
          "uploads": "string"
        }
      },
      "etag": "string",
      "id": "string",
      "kind": "string",
      "snippet": {
        "customUrl": "https://example.com",
        "description": "string",
        "publishedAt": "2026-05-07T12:00:00.000Z",
        "title": "string"
      },
      "statistics": {
        "subscriberCount": "string",
        "videoCount": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentDetails.relatedPlaylists.uploads` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `snippet.customUrl` | string |  |
| `snippet.description` | string |  |
| `snippet.publishedAt` | date |  |
| `snippet.title` | string |  |
| `statistics.subscriberCount` | string |  |
| `statistics.videoCount` | string |  |

## Native endpoint

Through the native YouTube API, this operation is `GET /youtube/v3/channels` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.


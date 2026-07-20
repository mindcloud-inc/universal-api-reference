# YouTube: List Playlist Items

Retrieves items from a YouTube playlist.

```
GET https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-playlist-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-playlist-items?connectionId=$CONNECTION_ID&limit=25&offset=0&part=snippet%2CcontentDetails%2Cstatus" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "part": "snippet,contentDetails,status"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-playlist-items?${params}`, {
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
| `part` | string | yes | Response parts to include. Default: `snippet,contentDetails,status`. |
| `playlistId` | string | no | The playlist ID to list items for. |
| `id` | string | no | Comma-separated playlist item IDs. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentDetails": {
        "videoId": "string",
        "videoPublishedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "snippet": {
        "description": "string",
        "position": 1,
        "resourceId": {
          "videoId": "string"
        },
        "title": "string"
      },
      "status": {
        "privacyStatus": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentDetails.videoId` | string |  |
| `contentDetails.videoPublishedAt` | date |  |
| `id` | string |  |
| `snippet.description` | string |  |
| `snippet.position` | number |  |
| `snippet.resourceId.videoId` | string |  |
| `snippet.title` | string |  |
| `status.privacyStatus` | string |  |

## Native endpoint

Through the native YouTube API, this operation is `GET /youtube/v3/playlistItems` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-playlist-items.md) for the provider-specific parameters and requirements.


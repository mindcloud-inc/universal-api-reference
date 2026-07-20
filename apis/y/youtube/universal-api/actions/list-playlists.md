# YouTube: List Playlists

Retrieves one or more playlists from YouTube.

```
GET https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-playlists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-playlists?connectionId=$CONNECTION_ID&limit=25&offset=0&part=snippet%2CcontentDetails%2Cstatus" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "part": "snippet,contentDetails,status"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-playlists?${params}`, {
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
| `channelId` | string | no | Return playlists for a channel. |
| `id` | string | no | Comma-separated playlist IDs. Accepts multiple values in one string, delimited by `,`. |
| `mine` | boolean | no | Return playlists owned by the authenticated YouTube channel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentDetails": {
        "itemCount": 1
      },
      "id": "string",
      "snippet": {
        "channelTitle": "string",
        "description": "string",
        "publishedAt": "2026-05-07T12:00:00.000Z",
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
| `contentDetails.itemCount` | number |  |
| `id` | string |  |
| `snippet.channelTitle` | string |  |
| `snippet.description` | string |  |
| `snippet.publishedAt` | date |  |
| `snippet.title` | string |  |
| `status.privacyStatus` | string |  |

## Native endpoint

Through the native YouTube API, this operation is `GET /youtube/v3/playlists` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-playlists.md) for the provider-specific parameters and requirements.


# YouTube: Create Playlist

Creates a new playlist in YouTube.

```
POST https://connect.mindcloud.co/v1/universal/youtube/latest/actions/create-playlist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/create-playlist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "part": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youtube/latest/actions/create-playlist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "part": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `part` | string | yes | Comma-separated playlist resource parts to include in the response and update. |
| `title` | string | yes | Playlist title. |
| `description` | string | no | Playlist description. |
| `privacyStatus` | string | no | Playlist visibility status. |
| `tags[]` | array<string> | no | Playlist tags. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `onBehalfOfContentOwner` | string | no | Content owner ID when acting on behalf of a CMS user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentDetails": {
        "itemCount": 1
      },
      "etag": "string",
      "id": "string",
      "kind": "string",
      "player": {
        "embedHtml": "string"
      },
      "snippet": {
        "channelTitle": "string",
        "description": "string",
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
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `player.embedHtml` | string |  |
| `snippet.channelTitle` | string |  |
| `snippet.description` | string |  |
| `snippet.title` | string |  |
| `status.privacyStatus` | string |  |

## Native endpoint

Through the native YouTube API, this operation is `POST /youtube/v3/playlists` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-playlist.md) for the provider-specific parameters and requirements.


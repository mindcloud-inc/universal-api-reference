# Invidious: Add Video To Auth Playlist



```
POST https://connect.mindcloud.co/v1/universal/invidious/latest/actions/add-video-to-auth-playlist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/add-video-to-auth-playlist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "IVPAAAAAAA",
  "videoId": "dQw4w9WgXcQ"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invidious/latest/actions/add-video-to-auth-playlist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "IVPAAAAAAA",
    "videoId": "dQw4w9WgXcQ"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Authenticated playlist ID. Example: `IVPAAAAAAA`. |
| `videoId` | string | yes | Video ID to add to the playlist. Example: `dQw4w9WgXcQ`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "playlistId": "string",
      "success": true,
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `playlistId` | string |  |
| `success` | boolean |  |
| `videoId` | string |  |

## Native endpoint

Through the native Invidious API, this operation is `POST /auth/playlists/:id/videos` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-video-to-auth-playlist.md) for the provider-specific parameters and requirements.


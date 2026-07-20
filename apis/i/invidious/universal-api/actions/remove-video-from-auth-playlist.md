# Invidious: Remove Video From Auth Playlist



```
DELETE https://connect.mindcloud.co/v1/universal/invidious/latest/actions/remove-video-from-auth-playlist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/remove-video-from-auth-playlist?connectionId=$CONNECTION_ID&id=IVPAAAAAAA&index=playlist-index-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "IVPAAAAAAA",
  "index": "playlist-index-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/remove-video-from-auth-playlist?${params}`, {
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
| `id` | string | yes | Authenticated playlist ID. Example: `IVPAAAAAAA`. |
| `index` | string | yes | Playlist video indexId to remove. Example: `playlist-index-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "index": "string",
      "message": "string",
      "playlistId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `index` | string |  |
| `message` | string |  |
| `playlistId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Invidious API, this operation is `DELETE /auth/playlists/:id/videos/:index` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-video-from-auth-playlist.md) for the provider-specific parameters and requirements.


# Invidious: Update Auth Playlist



```
PUT https://connect.mindcloud.co/v1/universal/invidious/latest/actions/update-auth-playlist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/update-auth-playlist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "IVPAAAAAAA"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invidious/latest/actions/update-auth-playlist', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "IVPAAAAAAA"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | New playlist description. |
| `id` | string | yes | Authenticated playlist ID. Example: `IVPAAAAAAA`. |
| `privacy` | string | no | Playlist privacy: public, unlisted, or private. |
| `title` | string | no | New playlist title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "playlistId": "string",
      "privacy": "string",
      "success": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `playlistId` | string |  |
| `privacy` | string |  |
| `success` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native Invidious API, this operation is `PATCH /auth/playlists/:id` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-auth-playlist.md) for the provider-specific parameters and requirements.


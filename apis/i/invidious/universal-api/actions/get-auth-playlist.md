# Invidious: Get Auth Playlist



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-auth-playlist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-auth-playlist?connectionId=$CONNECTION_ID&id=IVPAAAAAAA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "IVPAAAAAAA"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-auth-playlist?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "playlistId": "string",
      "title": "string",
      "videoCount": 1,
      "videos": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `playlistId` | string |  |
| `title` | string |  |
| `videoCount` | number |  |
| `videos` | array<object> |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /auth/playlists/:id` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-auth-playlist.md) for the provider-specific parameters and requirements.


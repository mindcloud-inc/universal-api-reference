# Invidious: Get Playlist



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-playlist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-playlist?connectionId=$CONNECTION_ID&playlistId=PL1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "playlistId": "PL1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-playlist?${params}`, {
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
| `page` | number | no | Playlist page number. Example: `1`. |
| `playlistId` | string | yes | Playlist ID. Example: `PL1234567890`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "authorId": "string",
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
| `author` | string |  |
| `authorId` | string |  |
| `playlistId` | string |  |
| `title` | string |  |
| `videoCount` | number |  |
| `videos` | array<object> |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /playlists/:plid` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-playlist.md) for the provider-specific parameters and requirements.


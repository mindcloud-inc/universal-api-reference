# VideoDB: List Videos

Retrieves videos from VideoDB.

```
GET https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/list-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VideoDB `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/list-videos?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/list-videos?${params}`, {
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
| `collectionId` | string | no | Collection to scope the video list. Defaults to the built-in default collection. Default: `default`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collection_id": "string",
      "id": "string",
      "length": "string",
      "name": "Ava Chen",
      "player_link": "https://example.com",
      "player_url": "https://example.com",
      "size": "string",
      "stream_link": "https://example.com",
      "stream_url": "https://example.com",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection_id` | string | Collection identifier. |
| `id` | string | Video identifier. |
| `length` | string | Video length as returned by VideoDB. |
| `name` | string | Video name. |
| `player_link` | string | Player link. |
| `player_url` | string | Player URL. |
| `size` | string | Video size as returned by VideoDB. |
| `stream_link` | string | Stream link. |
| `stream_url` | string | Stream URL. |
| `user_id` | string | Owner identifier. |

## Native endpoint

Through the native VideoDB API, this operation is `GET /video/` (base URL `https://api.videodb.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-videos.md) for the provider-specific parameters and requirements.


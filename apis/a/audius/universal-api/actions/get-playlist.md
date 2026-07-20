# Audius: Get Playlist

Retrieves a playlist from Audius by ID.

```
GET https://connect.mindcloud.co/v1/universal/audius/latest/actions/get-playlist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Audius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/audius/latest/actions/get-playlist?connectionId=$CONNECTION_ID&playlistId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "playlistId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/audius/latest/actions/get-playlist?${params}`, {
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
| `playlistId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Audius API returns.

## Native endpoint

Through the native Audius API, this operation is `GET /playlists/:playlist_id` (base URL `https://api.audius.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-playlist.md) for the provider-specific parameters and requirements.


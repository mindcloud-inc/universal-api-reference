# Grafana: Get Playlist

Retrieves a playlist from Grafana.

```
GET https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-playlist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grafana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-playlist?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-playlist?${params}`, {
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
| `uid` | string | yes | The playlist UID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "interval": "string",
      "name": "Ava Chen",
      "type": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `interval` | string |  |
| `name` | string |  |
| `type` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Grafana API, this operation is `GET /playlists/:uid` (base URL `https://apps78aa.grafana.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-playlist.md) for the provider-specific parameters and requirements.


# Twitch: List Top Games

Retrieves top game categories from Twitch.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-top-games
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-top-games?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-top-games?${params}`, {
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
| `first` | number | no | The maximum number of objects to return. Maximum: 100. Default: 20. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `after` | string | no | The cursor used to get the next page of results. |
| `before` | string | no | The cursor used to get the previous page of results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "boxArtUrl": "https://example.com",
      "id": "string",
      "igdbId": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `boxArtUrl` | string |  |
| `id` | string |  |
| `igdbId` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Twitch API, this operation is `GET /games/top` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-top-games.md) for the provider-specific parameters and requirements.


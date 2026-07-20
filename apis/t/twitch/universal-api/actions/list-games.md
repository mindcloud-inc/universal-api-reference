# Twitch: List Games

Retrieves game category records from Twitch.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-games
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-games?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-games?${params}`, {
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
| `id` | string | no | The ID of the game to get. Specify this parameter up to 100 times. Accepts multiple values as an array. |
| `name` | string | no | The name of the game to get. Specify this parameter up to 100 times. Accepts multiple values as an array. |
| `igdbId` | string | no | The IGDB ID of the game to get. Specify this parameter up to 100 times. Accepts multiple values as an array. |

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

Through the native Twitch API, this operation is `GET /games` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-games.md) for the provider-specific parameters and requirements.


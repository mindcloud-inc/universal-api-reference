# Scoreboard Buzz: List Games

Retrieves games from Scoreboard Buzz.

```
GET https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-games
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoreboard Buzz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-games?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-games?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Scoreboard Buzz game ID. |
| `name` | string | Game name. |

## Native endpoint

Through the native Scoreboard Buzz API, this operation is `GET /games` (base URL `https://api.scoreboardbuzz.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-games.md) for the provider-specific parameters and requirements.


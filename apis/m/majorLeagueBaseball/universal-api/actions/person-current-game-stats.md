# Major League Baseball: Person View a players stats



```
GET https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/person-current-game-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Major League Baseball `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/person-current-game-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/person-current-game-stats?${params}`, {
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
      "leaders": "string",
      "splits": "string",
      "stats": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `leaders` | string |  |
| `splits` | string |  |
| `stats` | string |  |

## Native endpoint

Through the native Major League Baseball API, this operation is `GET /v1/people/{personId}/stats/game/current` (base URL `https://statsapi.mlb.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/person-current-game-stats.md) for the provider-specific parameters and requirements.


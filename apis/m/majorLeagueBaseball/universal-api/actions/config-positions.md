# Major League Baseball: List all possible positions



```
GET https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/config-positions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Major League Baseball `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/config-positions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/config-positions?${params}`, {
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
      "abbreviation": "string",
      "code": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abbreviation` | string |  |
| `code` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Major League Baseball API, this operation is `GET /v1/positions` (base URL `https://statsapi.mlb.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/config-positions.md) for the provider-specific parameters and requirements.


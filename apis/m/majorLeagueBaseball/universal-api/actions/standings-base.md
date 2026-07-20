# Major League Baseball: View standings



```
GET https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/standings-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Major League Baseball `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/standings-base?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/standings-base?${params}`, {
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
      "division": "string",
      "league": "string",
      "sport": "string",
      "teamRecords": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `division` | string |  |
| `league` | string |  |
| `sport` | string |  |
| `teamRecords` | string |  |

## Native endpoint

Through the native Major League Baseball API, this operation is `GET /v1/standings` (base URL `https://statsapi.mlb.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/standings-base.md) for the provider-specific parameters and requirements.


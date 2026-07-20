# Major League Baseball: View a teams info



```
GET https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/team-roster
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Major League Baseball `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/team-roster?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/team-roster?${params}`, {
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
      "jerseyNumber": "string",
      "person": "string",
      "position": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jerseyNumber` | string |  |
| `person` | string |  |
| `position` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Major League Baseball API, this operation is `GET /v1/teams/{teamId}/roster/{rosterType}` (base URL `https://statsapi.mlb.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/team-roster.md) for the provider-specific parameters and requirements.


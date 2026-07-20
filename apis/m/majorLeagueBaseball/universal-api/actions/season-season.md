# Major League Baseball: Season View season info



```
GET https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/season-season
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Major League Baseball `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/season-season?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/majorLeagueBaseball/latest/actions/season-season?${params}`, {
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
      "regularSeasonEndDate": "string",
      "regularSeasonStartDate": "string",
      "seasonId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `regularSeasonEndDate` | string |  |
| `regularSeasonStartDate` | string |  |
| `seasonId` | string |  |

## Native endpoint

Through the native Major League Baseball API, this operation is `GET /v1/seasons/{seasonId}` (base URL `https://statsapi.mlb.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/season-season.md) for the provider-specific parameters and requirements.


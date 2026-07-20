# SportsData: NBA Current Season

Retrieves the current NBA season from SportsData.

```
GET https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-current-season
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SportsData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-current-season?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-current-season?${params}`, {
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
      "apiSeason": "string",
      "description": "string",
      "endYear": 1,
      "postSeasonStartDate": "2026-05-07T12:00:00.000Z",
      "regularSeasonStartDate": "2026-05-07T12:00:00.000Z",
      "season": 1,
      "seasonType": "string",
      "startYear": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiSeason` | string | Provider API season token. |
| `description` | string | Season label. |
| `endYear` | number | Season end year. |
| `postSeasonStartDate` | date | Postseason start date. |
| `regularSeasonStartDate` | date | Regular season start date. |
| `season` | number | Season year. |
| `seasonType` | string | Season type code. |
| `startYear` | number | Season start year. |

## Native endpoint

Through the native SportsData API, this operation is `GET /v3/nba/scores/json/CurrentSeason` (base URL `https://api.sportsdata.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nba-current-season.md) for the provider-specific parameters and requirements.


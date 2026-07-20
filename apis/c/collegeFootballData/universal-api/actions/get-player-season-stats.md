# College Football Data: List Player Season Stats

Retrieves player season statistics from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-player-season-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-player-season-stats?connectionId=$CONNECTION_ID&year=2025" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2025"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-player-season-stats?${params}`, {
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
| `year` | number | yes | Required year filter Default: `2025`. |
| `conference` | string | no | Optional conference filter |
| `team` | string | no | Optional team filter |
| `startWeek` | number | no | Optional starting week range |
| `endWeek` | number | no | Optional ending week range |
| `seasonType` | string | no | Optional season type filter |
| `category` | string | no | Optional category filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "conference": "string",
      "player": "string",
      "playerId": "string",
      "position": "string",
      "season": 1,
      "stat": "string",
      "statType": "string",
      "team": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `conference` | string |  |
| `player` | string |  |
| `playerId` | string |  |
| `position` | string |  |
| `season` | number |  |
| `stat` | string |  |
| `statType` | string |  |
| `team` | string |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /stats/player/season` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-player-season-stats.md) for the provider-specific parameters and requirements.


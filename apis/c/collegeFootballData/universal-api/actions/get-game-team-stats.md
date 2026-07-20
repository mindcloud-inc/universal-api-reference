# College Football Data: List Game Team Stats

Retrieves team box score statistics from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-game-team-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-game-team-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-game-team-stats?${params}`, {
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
| `year` | number | no | Required year filter (along with one of week, team, or conference), unless id is specified |
| `week` | number | no | Optional week filter, required if team and conference not specified |
| `team` | string | no | Optional team filter, required if week and conference not specified |
| `conference` | string | no | Optional conference filter, required if week and team not specified |
| `classification` | string | no | Optional division classification filter |
| `seasonType` | string | no | Optional season type filter |
| `id` | number | no | Optional id filter to retrieve a single game |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "teams": {
        "conference": "string",
        "homeAway": "string",
        "points": 1,
        "stats": {
          "category": "string",
          "stat": "string"
        },
        "team": "string",
        "teamId": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `teams.conference` | string |  |
| `teams.homeAway` | string |  |
| `teams.points` | number |  |
| `teams.stats.category` | string |  |
| `teams.stats.stat` | string |  |
| `teams.team` | string |  |
| `teams.teamId` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /games/teams` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-game-team-stats.md) for the provider-specific parameters and requirements.


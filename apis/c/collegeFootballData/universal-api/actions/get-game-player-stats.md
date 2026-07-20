# College Football Data: List Game Player Stats

Retrieves player box score statistics from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-game-player-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-game-player-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-game-player-stats?${params}`, {
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
| `category` | string | no | Optional player statistical category filter |
| `id` | number | no | Optional id filter to retrieve a single game |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "teams": {
        "categories": {
          "name": "Ava Chen",
          "types": {
            "athletes": {
              "id": "string",
              "name": "Ava Chen",
              "stat": "string"
            },
            "name": "Ava Chen"
          }
        },
        "conference": "string",
        "homeAway": "string",
        "points": 1,
        "team": "string"
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
| `teams.categories.name` | string |  |
| `teams.categories.types.athletes.id` | string |  |
| `teams.categories.types.athletes.name` | string |  |
| `teams.categories.types.athletes.stat` | string |  |
| `teams.categories.types.name` | string |  |
| `teams.conference` | string |  |
| `teams.homeAway` | string |  |
| `teams.points` | number |  |
| `teams.team` | string |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /games/players` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-game-player-stats.md) for the provider-specific parameters and requirements.


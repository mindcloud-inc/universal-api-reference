# College Football Data: List Predicted Points Added By Player Game

Retrieves player PPA statistics by game from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-predicted-points-added-by-player-game
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-predicted-points-added-by-player-game?connectionId=$CONNECTION_ID&year=2025" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2025"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-predicted-points-added-by-player-game?${params}`, {
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
| `week` | number | no | Week filter, required if team not specified |
| `seasonType` | string | no | Optional season type filter |
| `team` | string | no | Team filter, required if week not specified |
| `position` | string | no | Optional player position abbreviation filter |
| `playerId` | string | no | Optional player ID filter |
| `threshold` | number | no | Threshold value for minimum number of plays |
| `excludeGarbageTime` | boolean | no | Optional flag to exclude garbage time plays |

## Response

```json
{
  "success": true,
  "data": [
    {
      "averagePPA": {
        "all": 1,
        "pass": 1,
        "rush": 1
      },
      "id": "string",
      "name": "Ava Chen",
      "opponent": "string",
      "position": "string",
      "season": 1,
      "seasonType": "string",
      "team": "string",
      "week": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averagePPA.all` | number |  |
| `averagePPA.pass` | number |  |
| `averagePPA.rush` | number |  |
| `id` | string |  |
| `name` | string |  |
| `opponent` | string |  |
| `position` | string |  |
| `season` | number |  |
| `seasonType` | string |  |
| `team` | string |  |
| `week` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /ppa/players/games` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-predicted-points-added-by-player-game.md) for the provider-specific parameters and requirements.


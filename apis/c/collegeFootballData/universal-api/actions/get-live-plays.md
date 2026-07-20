# College Football Data: Get Live Plays

Retrieves live play-by-play data from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-live-plays
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-live-plays?connectionId=$CONNECTION_ID&gameId=401756846" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "gameId": "401756846"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-live-plays?${params}`, {
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
| `gameId` | number | yes | Game Id filter Default: `401756846`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clock": "string",
      "distance": 1,
      "down": 1,
      "drives": {
        "defense": "string",
        "defenseId": 1,
        "duration": "string",
        "endClock": "string",
        "endPeriod": 1,
        "endYardsToGoal": 1,
        "id": "string",
        "offense": "string",
        "offenseId": 1,
        "playCount": 1,
        "plays": {
          "awayScore": 1,
          "clock": "string",
          "distance": 1,
          "down": 1,
          "downType": "string",
          "epa": 1,
          "garbageTime": true,
          "homeScore": 1,
          "id": "string",
          "period": 1,
          "playText": "string",
          "playType": "string",
          "playTypeId": 1,
          "rushPass": "string",
          "success": true,
          "team": "string",
          "teamId": 1,
          "wallClock": "string",
          "yardsGained": 1,
          "yardsToGoal": 1
        },
        "pointsGained": 1,
        "result": "string",
        "scoringOpportunity": true,
        "startClock": "string",
        "startPeriod": 1,
        "startYardsToGoal": 1,
        "yards": 1
      },
      "id": 1,
      "period": 1,
      "possession": "string",
      "status": "string",
      "teams": {
        "averageStartYardLine": 1,
        "deserveToWin": 1,
        "drives": 1,
        "epaPerPass": 1,
        "epaPerPlay": 1,
        "epaPerRush": 1,
        "explosiveness": 1,
        "homeAway": "string",
        "lineScores": [
          1
        ],
        "lineYards": 1,
        "lineYardsPerRush": 1,
        "openFieldYards": 1,
        "openFieldYardsPerRush": 1,
        "passingDownSuccessRate": 1,
        "passingEpa": 1,
        "plays": 1,
        "points": 1,
        "pointsPerOpportunity": 1,
        "rushingEpa": 1,
        "scoringOpportunities": 1,
        "secondLevelYards": 1,
        "secondLevelYardsPerRush": 1,
        "standardDownSuccessRate": 1,
        "successRate": 1,
        "team": "string",
        "teamId": 1,
        "totalEpa": 1
      },
      "yardsToGoal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clock` | string |  |
| `distance` | number |  |
| `down` | number |  |
| `drives.defense` | string |  |
| `drives.defenseId` | number |  |
| `drives.duration` | string |  |
| `drives.endClock` | string |  |
| `drives.endPeriod` | number |  |
| `drives.endYardsToGoal` | number |  |
| `drives.id` | string |  |
| `drives.offense` | string |  |
| `drives.offenseId` | number |  |
| `drives.playCount` | number |  |
| `drives.plays.awayScore` | number |  |
| `drives.plays.clock` | string |  |
| `drives.plays.distance` | number |  |
| `drives.plays.down` | number |  |
| `drives.plays.downType` | string |  |
| `drives.plays.epa` | number |  |
| `drives.plays.garbageTime` | boolean |  |
| `drives.plays.homeScore` | number |  |
| `drives.plays.id` | string |  |
| `drives.plays.period` | number |  |
| `drives.plays.playText` | string |  |
| `drives.plays.playType` | string |  |
| `drives.plays.playTypeId` | number |  |
| `drives.plays.rushPass` | string |  |
| `drives.plays.success` | boolean |  |
| `drives.plays.team` | string |  |
| `drives.plays.teamId` | number |  |
| `drives.plays.wallClock` | string |  |
| `drives.plays.yardsGained` | number |  |
| `drives.plays.yardsToGoal` | number |  |
| `drives.pointsGained` | number |  |
| `drives.result` | string |  |
| `drives.scoringOpportunity` | boolean |  |
| `drives.startClock` | string |  |
| `drives.startPeriod` | number |  |
| `drives.startYardsToGoal` | number |  |
| `drives.yards` | number |  |
| `id` | number |  |
| `period` | number |  |
| `possession` | string |  |
| `status` | string |  |
| `teams.averageStartYardLine` | number |  |
| `teams.deserveToWin` | number |  |
| `teams.drives` | number |  |
| `teams.epaPerPass` | number |  |
| `teams.epaPerPlay` | number |  |
| `teams.epaPerRush` | number |  |
| `teams.explosiveness` | number |  |
| `teams.homeAway` | string |  |
| `teams.lineScores` | array<number> |  |
| `teams.lineYards` | number |  |
| `teams.lineYardsPerRush` | number |  |
| `teams.openFieldYards` | number |  |
| `teams.openFieldYardsPerRush` | number |  |
| `teams.passingDownSuccessRate` | number |  |
| `teams.passingEpa` | number |  |
| `teams.plays` | number |  |
| `teams.points` | number |  |
| `teams.pointsPerOpportunity` | number |  |
| `teams.rushingEpa` | number |  |
| `teams.scoringOpportunities` | number |  |
| `teams.secondLevelYards` | number |  |
| `teams.secondLevelYardsPerRush` | number |  |
| `teams.standardDownSuccessRate` | number |  |
| `teams.successRate` | number |  |
| `teams.team` | string |  |
| `teams.teamId` | number |  |
| `teams.totalEpa` | number |  |
| `yardsToGoal` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /live/plays` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-live-plays.md) for the provider-specific parameters and requirements.


# College Football Data: List Play Stats

Retrieves player-play associations from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-play-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-play-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-play-stats?${params}`, {
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
| `year` | number | no | Optional year filter |
| `week` | number | no | Optional week filter |
| `team` | string | no | Optional team filter |
| `gameId` | number | no | Optional gameId filter |
| `athleteId` | number | no | Optional athleteId filter |
| `statTypeId` | number | no | Optional statTypeId filter |
| `seasonType` | string | no | Optional season type filter |
| `conference` | string | no | Optional conference filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "athleteId": "string",
      "athleteName": "Ava Chen",
      "clock": {
        "minutes": 1,
        "seconds": 1
      },
      "conference": "string",
      "distance": 1,
      "down": 1,
      "driveId": "string",
      "gameId": 1,
      "opponent": "string",
      "opponentScore": 1,
      "period": 1,
      "playId": "string",
      "season": 1,
      "stat": 1,
      "statType": "string",
      "team": "string",
      "teamScore": 1,
      "week": 1,
      "yardsToGoal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `athleteId` | string |  |
| `athleteName` | string |  |
| `clock.minutes` | number |  |
| `clock.seconds` | number |  |
| `conference` | string |  |
| `distance` | number |  |
| `down` | number |  |
| `driveId` | string |  |
| `gameId` | number |  |
| `opponent` | string |  |
| `opponentScore` | number |  |
| `period` | number |  |
| `playId` | string |  |
| `season` | number |  |
| `stat` | number |  |
| `statType` | string |  |
| `team` | string |  |
| `teamScore` | number |  |
| `week` | number |  |
| `yardsToGoal` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /plays/stats` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-play-stats.md) for the provider-specific parameters and requirements.


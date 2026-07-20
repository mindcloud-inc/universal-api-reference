# College Football Data: List Drives

Retrieves historical drives from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-drives
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-drives?connectionId=$CONNECTION_ID&year=2025" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2025"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-drives?${params}`, {
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
| `seasonType` | string | no | Optional season type filter |
| `week` | number | no | Optional week filter |
| `team` | string | no | Optional team filter |
| `offense` | string | no | Optional offensive team filter |
| `defense` | string | no | Optional defensive team filter |
| `conference` | string | no | Optional conference filter |
| `offenseConference` | string | no | Optional offensive team conference filter |
| `defenseConference` | string | no | Optional defensive team conference filter |
| `classification` | string | no | Optional division classification filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defense": "string",
      "defenseConference": "string",
      "driveNumber": 1,
      "driveResult": "string",
      "elapsed": {
        "minutes": 1,
        "seconds": 1
      },
      "endDefenseScore": 1,
      "endOffenseScore": 1,
      "endPeriod": 1,
      "endTime": {
        "minutes": 1,
        "seconds": 1
      },
      "endYardline": 1,
      "endYardsToGoal": 1,
      "gameId": 1,
      "id": "string",
      "isHomeOffense": true,
      "offense": "string",
      "offenseConference": "string",
      "plays": 1,
      "scoring": true,
      "startDefenseScore": 1,
      "startOffenseScore": 1,
      "startPeriod": 1,
      "startTime": {
        "minutes": 1,
        "seconds": 1
      },
      "startYardline": 1,
      "startYardsToGoal": 1,
      "yards": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defense` | string |  |
| `defenseConference` | string |  |
| `driveNumber` | number |  |
| `driveResult` | string |  |
| `elapsed.minutes` | number |  |
| `elapsed.seconds` | number |  |
| `endDefenseScore` | number |  |
| `endOffenseScore` | number |  |
| `endPeriod` | number |  |
| `endTime.minutes` | number |  |
| `endTime.seconds` | number |  |
| `endYardline` | number |  |
| `endYardsToGoal` | number |  |
| `gameId` | number |  |
| `id` | string |  |
| `isHomeOffense` | boolean |  |
| `offense` | string |  |
| `offenseConference` | string |  |
| `plays` | number |  |
| `scoring` | boolean |  |
| `startDefenseScore` | number |  |
| `startOffenseScore` | number |  |
| `startPeriod` | number |  |
| `startTime.minutes` | number |  |
| `startTime.seconds` | number |  |
| `startYardline` | number |  |
| `startYardsToGoal` | number |  |
| `yards` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /drives` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-drives.md) for the provider-specific parameters and requirements.


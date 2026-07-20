# College Football Data: List Plays

Retrieves historical plays from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-plays
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-plays?connectionId=$CONNECTION_ID&year=2025&week=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2025",
  "week": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-plays?${params}`, {
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
| `week` | number | yes | Required week filter Default: `1`. |
| `team` | string | no | Optional team filter |
| `offense` | string | no | Optional offensive team filter |
| `defense` | string | no | Optional defensive team filter |
| `offenseConference` | string | no | Optional offensive conference filter |
| `defenseConference` | string | no | Optional defensive conference filter |
| `conference` | string | no | Optional conference filter |
| `playType` | string | no | Optoinal play type abbreviation filter |
| `seasonType` | string | no | Optional season type filter |
| `classification` | string | no | Optional division classification filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "away": "string",
      "clock": {
        "minutes": 1,
        "seconds": 1
      },
      "defense": "string",
      "defenseConference": "string",
      "defenseScore": 1,
      "defenseTimeouts": 1,
      "distance": 1,
      "down": 1,
      "driveId": "string",
      "driveNumber": 1,
      "gameId": 1,
      "home": "string",
      "id": "string",
      "offense": "string",
      "offenseConference": "string",
      "offenseScore": 1,
      "offenseTimeouts": 1,
      "period": 1,
      "playNumber": 1,
      "playText": "string",
      "playType": "string",
      "ppa": 1,
      "scoring": true,
      "wallclock": "string",
      "yardline": 1,
      "yardsGained": 1,
      "yardsToGoal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `away` | string |  |
| `clock.minutes` | number |  |
| `clock.seconds` | number |  |
| `defense` | string |  |
| `defenseConference` | string |  |
| `defenseScore` | number |  |
| `defenseTimeouts` | number |  |
| `distance` | number |  |
| `down` | number |  |
| `driveId` | string |  |
| `driveNumber` | number |  |
| `gameId` | number |  |
| `home` | string |  |
| `id` | string |  |
| `offense` | string |  |
| `offenseConference` | string |  |
| `offenseScore` | number |  |
| `offenseTimeouts` | number |  |
| `period` | number |  |
| `playNumber` | number |  |
| `playText` | string |  |
| `playType` | string |  |
| `ppa` | number |  |
| `scoring` | boolean |  |
| `wallclock` | string |  |
| `yardline` | number |  |
| `yardsGained` | number |  |
| `yardsToGoal` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /plays` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-plays.md) for the provider-specific parameters and requirements.


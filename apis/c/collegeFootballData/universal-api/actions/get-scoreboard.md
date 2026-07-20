# College Football Data: List Scoreboard

Retrieves live scoreboard data from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-scoreboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-scoreboard?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-scoreboard?${params}`, {
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
| `classification` | string | no | Optional division classification filter, defaults to fbs |
| `conference` | string | no | Optional conference filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "awayTeam": {
        "classification": "string",
        "conference": "string",
        "id": 1,
        "lineScores": [
          1
        ],
        "name": "Ava Chen",
        "points": 1,
        "winProbability": 1
      },
      "betting": {
        "awayMoneyline": 1,
        "homeMoneyline": 1,
        "overUnder": 1,
        "spread": 1
      },
      "clock": "string",
      "conferenceGame": true,
      "homeTeam": {
        "classification": "string",
        "conference": "string",
        "id": 1,
        "lineScores": [
          1
        ],
        "name": "Ava Chen",
        "points": 1,
        "winProbability": 1
      },
      "id": 1,
      "lastPlay": "string",
      "neutralSite": true,
      "period": 1,
      "possession": "string",
      "situation": "string",
      "startDate": "string",
      "startTimeTBD": true,
      "status": "string",
      "tv": "string",
      "venue": {
        "city": "string",
        "name": "Ava Chen",
        "state": "string"
      },
      "weather": {
        "description": "string",
        "temperature": 1,
        "windDirection": 1,
        "windSpeed": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `awayTeam.classification` | string |  |
| `awayTeam.conference` | string |  |
| `awayTeam.id` | number |  |
| `awayTeam.lineScores` | array<number> |  |
| `awayTeam.name` | string |  |
| `awayTeam.points` | number |  |
| `awayTeam.winProbability` | number |  |
| `betting.awayMoneyline` | number |  |
| `betting.homeMoneyline` | number |  |
| `betting.overUnder` | number |  |
| `betting.spread` | number |  |
| `clock` | string |  |
| `conferenceGame` | boolean |  |
| `homeTeam.classification` | string |  |
| `homeTeam.conference` | string |  |
| `homeTeam.id` | number |  |
| `homeTeam.lineScores` | array<number> |  |
| `homeTeam.name` | string |  |
| `homeTeam.points` | number |  |
| `homeTeam.winProbability` | number |  |
| `id` | number |  |
| `lastPlay` | string |  |
| `neutralSite` | boolean |  |
| `period` | number |  |
| `possession` | string |  |
| `situation` | string |  |
| `startDate` | string |  |
| `startTimeTBD` | boolean |  |
| `status` | string |  |
| `tv` | string |  |
| `venue.city` | string |  |
| `venue.name` | string |  |
| `venue.state` | string |  |
| `weather.description` | string |  |
| `weather.temperature` | number |  |
| `weather.windDirection` | number |  |
| `weather.windSpeed` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /scoreboard` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scoreboard.md) for the provider-specific parameters and requirements.


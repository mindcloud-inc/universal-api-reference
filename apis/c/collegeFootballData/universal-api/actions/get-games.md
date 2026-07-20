# College Football Data: List Games

Retrieves historical games from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-games
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-games?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-games?${params}`, {
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
| `year` | number | no | Required year filter (except when id is specified) |
| `week` | number | no | Optional week filter |
| `seasonType` | string | no | Optional season type filter |
| `classification` | string | no | Optional division classification filter |
| `team` | string | no | Optional team filter |
| `home` | string | no | Optional home team filter |
| `away` | string | no | Optional away team filter |
| `conference` | string | no | Optional conference filter |
| `id` | number | no | Game id filter to retrieve a single game |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendance": 1,
      "awayClassification": "string",
      "awayConference": "string",
      "awayId": 1,
      "awayLineScores": [
        1
      ],
      "awayPoints": 1,
      "awayPostgameElo": 1,
      "awayPostgameWinProbability": 1,
      "awayPregameElo": 1,
      "awayTeam": "string",
      "completed": true,
      "conferenceGame": true,
      "excitementIndex": 1,
      "highlights": "string",
      "homeClassification": "string",
      "homeConference": "string",
      "homeId": 1,
      "homeLineScores": [
        1
      ],
      "homePoints": 1,
      "homePostgameElo": 1,
      "homePostgameWinProbability": 1,
      "homePregameElo": 1,
      "homeTeam": "string",
      "id": 1,
      "neutralSite": true,
      "notes": "string",
      "season": 1,
      "seasonType": "string",
      "startDate": "string",
      "startTimeTBD": true,
      "venue": "string",
      "venueId": 1,
      "week": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendance` | number |  |
| `awayClassification` | string |  |
| `awayConference` | string |  |
| `awayId` | number |  |
| `awayLineScores` | array<number> |  |
| `awayPoints` | number |  |
| `awayPostgameElo` | number |  |
| `awayPostgameWinProbability` | number |  |
| `awayPregameElo` | number |  |
| `awayTeam` | string |  |
| `completed` | boolean |  |
| `conferenceGame` | boolean |  |
| `excitementIndex` | number |  |
| `highlights` | string |  |
| `homeClassification` | string |  |
| `homeConference` | string |  |
| `homeId` | number |  |
| `homeLineScores` | array<number> |  |
| `homePoints` | number |  |
| `homePostgameElo` | number |  |
| `homePostgameWinProbability` | number |  |
| `homePregameElo` | number |  |
| `homeTeam` | string |  |
| `id` | number |  |
| `neutralSite` | boolean |  |
| `notes` | string |  |
| `season` | number |  |
| `seasonType` | string |  |
| `startDate` | string |  |
| `startTimeTBD` | boolean |  |
| `venue` | string |  |
| `venueId` | number |  |
| `week` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /games` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-games.md) for the provider-specific parameters and requirements.


# College Football Data: Get Matchup

Retrieves historical team matchup details from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-matchup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-matchup?connectionId=$CONNECTION_ID&team1=Alabama&team2=Auburn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "team1": "Alabama",
  "team2": "Auburn"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-matchup?${params}`, {
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
| `team1` | string | yes | First team to compare Default: `Alabama`. |
| `team2` | string | yes | Second team to compare Default: `Auburn`. |
| `minYear` | number | no | Optional starting year |
| `maxYear` | number | no | Optional ending year |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endYear": 1,
      "games": {
        "awayScore": 1,
        "awayTeam": "string",
        "date": "string",
        "homeScore": 1,
        "homeTeam": "string",
        "neutralSite": true,
        "season": 1,
        "seasonType": "string",
        "venue": "string",
        "week": 1,
        "winner": "string"
      },
      "startYear": 1,
      "team1": "string",
      "team1Wins": 1,
      "team2": "string",
      "team2Wins": 1,
      "ties": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endYear` | number |  |
| `games.awayScore` | number |  |
| `games.awayTeam` | string |  |
| `games.date` | string |  |
| `games.homeScore` | number |  |
| `games.homeTeam` | string |  |
| `games.neutralSite` | boolean |  |
| `games.season` | number |  |
| `games.seasonType` | string |  |
| `games.venue` | string |  |
| `games.week` | number |  |
| `games.winner` | string |  |
| `startYear` | number |  |
| `team1` | string |  |
| `team1Wins` | number |  |
| `team2` | string |  |
| `team2Wins` | number |  |
| `ties` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /teams/matchup` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-matchup.md) for the provider-specific parameters and requirements.


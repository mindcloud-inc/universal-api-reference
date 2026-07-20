# SportsData: NBA Standings

Retrieves NBA standings from SportsData.

```
GET https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-standings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SportsData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-standings?connectionId=$CONNECTION_ID&season=2026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "season": "2026"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-standings?${params}`, {
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
| `season` | string | yes | NBA season year for standings. Example: `2026`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "awayLosses": 1,
      "awayWins": 1,
      "city": "string",
      "clinchedConference": true,
      "clinchedDivision": true,
      "clinchedPlayInTournamentBerth": true,
      "clinchedPlayoffBerth": true,
      "conference": "string",
      "conferenceLosses": 1,
      "conferenceRank": 1,
      "conferenceWins": 1,
      "division": "string",
      "divisionLosses": 1,
      "divisionRank": 1,
      "divisionWins": 1,
      "eliminatedFromPlayoffContention": true,
      "gamesBack": 1,
      "globalTeamID": 1,
      "homeLosses": 1,
      "homeWins": 1,
      "key": "string",
      "lastTenLosses": 1,
      "lastTenWins": 1,
      "losses": 1,
      "name": "Ava Chen",
      "percentage": 1,
      "pointsPerGameAgainst": 1,
      "pointsPerGameFor": 1,
      "season": 1,
      "seasonType": 1,
      "streak": 1,
      "streakDescription": "string",
      "teamID": 1,
      "wins": 1,
      "wonPlayInTournament": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `awayLosses` | number | Away losses. |
| `awayWins` | number | Away wins. |
| `city` | string | Team city. |
| `clinchedConference` | boolean | Whether the team clinched the conference. |
| `clinchedDivision` | boolean | Whether the team clinched the division. |
| `clinchedPlayInTournamentBerth` | boolean | Whether the team clinched a play-in berth. |
| `clinchedPlayoffBerth` | boolean | Whether the team clinched a playoff berth. |
| `conference` | string | Conference name. |
| `conferenceLosses` | number | Conference losses. |
| `conferenceRank` | number | Conference rank. |
| `conferenceWins` | number | Conference wins. |
| `division` | string | Division name. |
| `divisionLosses` | number | Division losses. |
| `divisionRank` | number | Division rank. |
| `divisionWins` | number | Division wins. |
| `eliminatedFromPlayoffContention` | boolean | Whether the team has been eliminated from playoff contention. |
| `gamesBack` | number | Games behind the conference leader. |
| `globalTeamID` | number | Global team identifier. |
| `homeLosses` | number | Home losses. |
| `homeWins` | number | Home wins. |
| `key` | string | Team abbreviation. |
| `lastTenLosses` | number | Losses over the last ten games. |
| `lastTenWins` | number | Wins over the last ten games. |
| `losses` | number | Losses. |
| `name` | string | Team name. |
| `percentage` | number | Winning percentage. |
| `pointsPerGameAgainst` | number | Points allowed per game. |
| `pointsPerGameFor` | number | Points scored per game. |
| `season` | number | Season year. |
| `seasonType` | number | SportsData season type code. |
| `streak` | number | Signed streak count. |
| `streakDescription` | string | Human-readable streak label. |
| `teamID` | number | Team identifier. |
| `wins` | number | Wins. |
| `wonPlayInTournament` | boolean | Whether the team advanced through the play-in tournament. |

## Native endpoint

Through the native SportsData API, this operation is `GET /v3/nba/scores/json/Standings/:season` (base URL `https://api.sportsdata.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nba-standings.md) for the provider-specific parameters and requirements.


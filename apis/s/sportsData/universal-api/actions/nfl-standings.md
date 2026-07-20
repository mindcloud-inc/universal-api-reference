# SportsData: NFL Standings

Retrieves NFL standings from SportsData.

```
GET https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-standings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SportsData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-standings?connectionId=$CONNECTION_ID&season=2025REG" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "season": "2025REG"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-standings?${params}`, {
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
| `season` | string | yes | NFL season year for standings. Example: `2025REG`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "awayLosses": 1,
      "awayWins": 1,
      "clinchedBye": true,
      "clinchedDivision": true,
      "clinchedWildCard": true,
      "conference": "string",
      "conferenceLosses": 1,
      "conferenceRank": 1,
      "conferenceWins": 1,
      "division": "string",
      "divisionLosses": 1,
      "divisionRank": 1,
      "divisionWins": 1,
      "eliminatedFromPlayoffContention": true,
      "globalTeamID": 1,
      "homeLosses": 1,
      "homeWins": 1,
      "losses": 1,
      "name": "Ava Chen",
      "netPoints": 1,
      "percentage": 1,
      "pointsAgainst": 1,
      "pointsFor": 1,
      "season": 1,
      "seasonType": 1,
      "streak": 1,
      "team": "string",
      "teamID": 1,
      "ties": 1,
      "touchdowns": 1,
      "wins": 1
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
| `clinchedBye` | boolean | Whether the team clinched a bye. |
| `clinchedDivision` | boolean | Whether the team clinched the division. |
| `clinchedWildCard` | boolean | Whether the team clinched a wild card berth. |
| `conference` | string | Conference name. |
| `conferenceLosses` | number | Conference losses. |
| `conferenceRank` | number | Conference rank. |
| `conferenceWins` | number | Conference wins. |
| `division` | string | Division name. |
| `divisionLosses` | number | Division losses. |
| `divisionRank` | number | Division rank. |
| `divisionWins` | number | Division wins. |
| `eliminatedFromPlayoffContention` | boolean | Whether the team has been eliminated from playoff contention. |
| `globalTeamID` | number | Global team identifier. |
| `homeLosses` | number | Home losses. |
| `homeWins` | number | Home wins. |
| `losses` | number | Losses. |
| `name` | string | Team display name. |
| `netPoints` | number | Point differential. |
| `percentage` | number | Winning percentage. |
| `pointsAgainst` | number | Points allowed. |
| `pointsFor` | number | Points scored. |
| `season` | number | Season year. |
| `seasonType` | number | SportsData season type code. |
| `streak` | number | Signed streak count. |
| `team` | string | Team abbreviation. |
| `teamID` | number | Team identifier. |
| `ties` | number | Ties. |
| `touchdowns` | number | Touchdowns scored. |
| `wins` | number | Wins. |

## Native endpoint

Through the native SportsData API, this operation is `GET /v3/nfl/scores/json/Standings/:season` (base URL `https://api.sportsdata.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nfl-standings.md) for the provider-specific parameters and requirements.


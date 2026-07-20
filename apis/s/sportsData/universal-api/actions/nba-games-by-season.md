# SportsData: NBA Games By Season

Retrieves NBA games from SportsData by season.

```
GET https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-games-by-season
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SportsData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-games-by-season?connectionId=$CONNECTION_ID&season=2026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "season": "2026"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-games-by-season?${params}`, {
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
| `season` | string | yes | NBA season year for the games feed. Example: `2026`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendance": 1,
      "awayTeam": "string",
      "awayTeamID": 1,
      "awayTeamMoneyLine": 1,
      "awayTeamScore": 1,
      "channel": "string",
      "crewChiefID": 1,
      "dateTime": "2026-05-07T12:00:00.000Z",
      "dateTimeUTC": "2026-05-07T12:00:00.000Z",
      "day": "2026-05-07T12:00:00.000Z",
      "gameEndDateTime": "2026-05-07T12:00:00.000Z",
      "gameID": 1,
      "globalAwayTeamID": 1,
      "globalGameID": 1,
      "globalHomeTeamID": 1,
      "homeTeam": "string",
      "homeTeamID": 1,
      "homeTeamMoneyLine": 1,
      "homeTeamScore": 1,
      "inseasonTournament": true,
      "isClosed": true,
      "lastPlay": "string",
      "neutralVenue": true,
      "overUnder": 1,
      "pointSpread": 1,
      "quarters": [
        {}
      ],
      "refereeID": 1,
      "season": 1,
      "seasonType": 1,
      "stadiumID": 1,
      "status": "string",
      "umpireID": 1,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendance` | number | Reported attendance. |
| `awayTeam` | string | Away team abbreviation. |
| `awayTeamID` | number | Away team identifier. |
| `awayTeamMoneyLine` | number | Away team moneyline. |
| `awayTeamScore` | number | Away team score. |
| `channel` | string | Broadcast channel. |
| `crewChiefID` | number | Crew chief identifier. |
| `dateTime` | date | Scheduled local game time. |
| `dateTimeUTC` | date | Scheduled UTC game time. |
| `day` | date | Calendar day for the game. |
| `gameEndDateTime` | date | Game end timestamp. |
| `gameID` | number | SportsData game identifier. |
| `globalAwayTeamID` | number | Global away team identifier. |
| `globalGameID` | number | Global game identifier. |
| `globalHomeTeamID` | number | Global home team identifier. |
| `homeTeam` | string | Home team abbreviation. |
| `homeTeamID` | number | Home team identifier. |
| `homeTeamMoneyLine` | number | Home team moneyline. |
| `homeTeamScore` | number | Home team score. |
| `inseasonTournament` | boolean | Whether the game is part of the in-season tournament. |
| `isClosed` | boolean | Whether the game is closed. |
| `lastPlay` | string | Most recent play summary. |
| `neutralVenue` | boolean | Whether the game is at a neutral venue. |
| `overUnder` | number | Over/under total. |
| `pointSpread` | number | Point spread for the game. |
| `quarters` | array<object> | Per-quarter scoring details when available. |
| `refereeID` | number | Referee identifier. |
| `season` | number | Season year for the game. |
| `seasonType` | number | SportsData season type code. |
| `stadiumID` | number | Venue identifier. |
| `status` | string | Current game status. |
| `umpireID` | number | Umpire identifier. |
| `updated` | date | Last provider update timestamp. |

## Native endpoint

Through the native SportsData API, this operation is `GET /v3/nba/scores/json/Games/:season` (base URL `https://api.sportsdata.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nba-games-by-season.md) for the provider-specific parameters and requirements.


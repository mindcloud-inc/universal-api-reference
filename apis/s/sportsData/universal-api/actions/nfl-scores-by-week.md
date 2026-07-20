# SportsData: NFL Scores By Week

Retrieves NFL scores from SportsData by week.

```
GET https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-scores-by-week
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SportsData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-scores-by-week?connectionId=$CONNECTION_ID&season=2025REG&week=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "season": "2025REG",
  "week": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-scores-by-week?${params}`, {
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
| `season` | string | yes | NFL season code for the scores feed, for example 2025REG. Example: `2025REG`. |
| `week` | string | yes | NFL week number within the selected season code. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendance": 1,
      "awayScore": 1,
      "awayTeam": "string",
      "awayTeamID": 1,
      "awayTeamMoneyLine": 1,
      "channel": "string",
      "closed": true,
      "date": "2026-05-07T12:00:00.000Z",
      "dateTime": "2026-05-07T12:00:00.000Z",
      "dateTimeUTC": "2026-05-07T12:00:00.000Z",
      "day": "2026-05-07T12:00:00.000Z",
      "forecastDescription": "string",
      "forecastTempHigh": 1,
      "forecastTempLow": 1,
      "gameEndDateTime": "2026-05-07T12:00:00.000Z",
      "gameKey": "string",
      "globalGameID": 1,
      "hasStarted": true,
      "homeScore": 1,
      "homeTeam": "string",
      "homeTeamID": 1,
      "homeTeamMoneyLine": 1,
      "isClosed": true,
      "isInProgress": true,
      "isOver": true,
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "neutralVenue": true,
      "overUnder": 1,
      "pointSpread": 1,
      "quarter": "string",
      "quarterDescription": "string",
      "refereeID": 1,
      "scoreID": 1,
      "season": 1,
      "seasonType": 1,
      "stadiumDetails": {},
      "stadiumID": 1,
      "status": "string",
      "week": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendance` | number | Reported attendance. |
| `awayScore` | number | Away team score. |
| `awayTeam` | string | Away team abbreviation. |
| `awayTeamID` | number | Away team identifier. |
| `awayTeamMoneyLine` | number | Away team moneyline. |
| `channel` | string | Broadcast channel. |
| `closed` | boolean | Whether the game is marked closed by the provider. |
| `date` | date | Scheduled local kickoff time. |
| `dateTime` | date | Scheduled local kickoff time. |
| `dateTimeUTC` | date | Scheduled UTC kickoff time. |
| `day` | date | Calendar day for the game. |
| `forecastDescription` | string | Game weather forecast description. |
| `forecastTempHigh` | number | Forecast high temperature. |
| `forecastTempLow` | number | Forecast low temperature. |
| `gameEndDateTime` | date | Game end timestamp. |
| `gameKey` | string | SportsData game key. |
| `globalGameID` | number | Global game identifier. |
| `hasStarted` | boolean | Whether the game has started. |
| `homeScore` | number | Home team score. |
| `homeTeam` | string | Home team abbreviation. |
| `homeTeamID` | number | Home team identifier. |
| `homeTeamMoneyLine` | number | Home team moneyline. |
| `isClosed` | boolean | Whether the game is closed. |
| `isInProgress` | boolean | Whether the game is live. |
| `isOver` | boolean | Whether the game is over. |
| `lastUpdated` | date | Last provider update timestamp. |
| `neutralVenue` | boolean | Whether the game is at a neutral venue. |
| `overUnder` | number | Over/under total. |
| `pointSpread` | number | Point spread for the game. |
| `quarter` | string | Current quarter or final state. |
| `quarterDescription` | string | Human-readable quarter status. |
| `refereeID` | number | Referee identifier. |
| `scoreID` | number | Score record identifier. |
| `season` | number | Season year for the game. |
| `seasonType` | number | SportsData season type code. |
| `stadiumDetails` | object | Nested stadium details for the game venue. |
| `stadiumID` | number | Venue identifier. |
| `status` | string | Current game status. |
| `week` | number | Week number for the game. |

## Native endpoint

Through the native SportsData API, this operation is `GET /v3/nfl/scores/json/ScoresByWeek/:season/:week` (base URL `https://api.sportsdata.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nfl-scores-by-week.md) for the provider-specific parameters and requirements.


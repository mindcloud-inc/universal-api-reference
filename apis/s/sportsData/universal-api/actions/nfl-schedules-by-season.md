# SportsData: NFL Schedules By Season

Retrieves NFL schedules from SportsData by season.

```
GET https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-schedules-by-season
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SportsData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-schedules-by-season?connectionId=$CONNECTION_ID&season=2026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "season": "2026"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-schedules-by-season?${params}`, {
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
| `season` | string | yes | NFL season year for the schedule feed. Example: `2026`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "awayTeam": "string",
      "awayTeamMoneyLine": 1,
      "canceled": true,
      "channel": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "dateTime": "2026-05-07T12:00:00.000Z",
      "dateTimeUTC": "2026-05-07T12:00:00.000Z",
      "day": "2026-05-07T12:00:00.000Z",
      "forecastDescription": "string",
      "forecastTempHigh": 1,
      "forecastTempLow": 1,
      "forecastWindChill": 1,
      "forecastWindSpeed": 1,
      "gameKey": "string",
      "globalAwayTeamID": 1,
      "globalGameID": 1,
      "globalHomeTeamID": 1,
      "homeTeam": "string",
      "homeTeamMoneyLine": 1,
      "overUnder": 1,
      "pointSpread": 1,
      "scoreID": 1,
      "season": 1,
      "seasonType": 1,
      "stadiumDetails": {
        "capacity": 1,
        "city": "string",
        "country": "string",
        "geoLat": 1,
        "geoLong": 1,
        "name": "Ava Chen",
        "playingSurface": "string",
        "stadiumID": 1,
        "state": "string",
        "type": "string"
      },
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
| `awayTeam` | string | Away team abbreviation. |
| `awayTeamMoneyLine` | number | Away team moneyline. |
| `canceled` | boolean | Whether the scheduled game was canceled. |
| `channel` | string | Broadcast channel. |
| `date` | date | Scheduled calendar date. |
| `dateTime` | date | Scheduled local kickoff time. |
| `dateTimeUTC` | date | Scheduled UTC kickoff time. |
| `day` | date | Calendar day bucket. |
| `forecastDescription` | string | Forecast summary. |
| `forecastTempHigh` | number | Forecast high temperature. |
| `forecastTempLow` | number | Forecast low temperature. |
| `forecastWindChill` | number | Forecast wind chill. |
| `forecastWindSpeed` | number | Forecast wind speed. |
| `gameKey` | string | Provider game key. |
| `globalAwayTeamID` | number | Global away team identifier. |
| `globalGameID` | number | Global game identifier. |
| `globalHomeTeamID` | number | Global home team identifier. |
| `homeTeam` | string | Home team abbreviation. |
| `homeTeamMoneyLine` | number | Home team moneyline. |
| `overUnder` | number | Game total. |
| `pointSpread` | number | Point spread. |
| `scoreID` | number | SportsData score identifier. |
| `season` | number | Season year for the schedule entry. |
| `seasonType` | number | SportsData season type code. |
| `stadiumDetails.capacity` | number | Venue capacity. |
| `stadiumDetails.city` | string | Venue city. |
| `stadiumDetails.country` | string | Venue country. |
| `stadiumDetails.geoLat` | number | Venue latitude. |
| `stadiumDetails.geoLong` | number | Venue longitude. |
| `stadiumDetails.name` | string | Venue name. |
| `stadiumDetails.playingSurface` | string | Playing surface. |
| `stadiumDetails.stadiumID` | number | Nested venue identifier. |
| `stadiumDetails.state` | string | Venue state or region. |
| `stadiumDetails.type` | string | Venue type. |
| `stadiumID` | number | Venue identifier. |
| `status` | string | Schedule status label. |
| `week` | number | Week number within the season. |

## Native endpoint

Through the native SportsData API, this operation is `GET /v3/nfl/scores/json/Schedules/:season` (base URL `https://api.sportsdata.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nfl-schedules-by-season.md) for the provider-specific parameters and requirements.


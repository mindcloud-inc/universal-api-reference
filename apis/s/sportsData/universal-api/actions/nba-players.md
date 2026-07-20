# SportsData: NBA Players

Retrieves active NBA player details from SportsData.

```
GET https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-players
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SportsData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-players?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-players?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "birthCity": "string",
      "birthCountry": "string",
      "birthDate": "2026-05-07T12:00:00.000Z",
      "birthState": "string",
      "college": "string",
      "depthChartOrder": 1,
      "depthChartPosition": "string",
      "draftKingsName": "Ava Chen",
      "draftKingsPlayerID": 1,
      "experience": 1,
      "fanDuelName": "Ava Chen",
      "fanDuelPlayerID": 1,
      "firstName": "Ava",
      "globalTeamID": 1,
      "height": 1,
      "jersey": 1,
      "lastName": "Chen",
      "nbaDotComPlayerID": 1,
      "photoUrl": "https://example.com",
      "playerID": 1,
      "position": "string",
      "positionCategory": "string",
      "salary": 1,
      "sportRadarPlayerID": "string",
      "status": "string",
      "team": "string",
      "teamID": 1,
      "usaTodayHeadshotNoBackgroundUrl": "https://example.com",
      "usaTodayHeadshotUrl": "https://example.com",
      "weight": 1,
      "yahooName": "Ava Chen",
      "yahooPlayerID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthCity` | string | Birth city. |
| `birthCountry` | string | Birth country. |
| `birthDate` | date | Player birth date. |
| `birthState` | string | Birth state or region. |
| `college` | string | College. |
| `depthChartOrder` | number | Depth chart order. |
| `depthChartPosition` | string | Depth chart position. |
| `draftKingsName` | string | DraftKings display name. |
| `draftKingsPlayerID` | number | DraftKings player identifier. |
| `experience` | number | Years of NBA experience. |
| `fanDuelName` | string | FanDuel display name. |
| `fanDuelPlayerID` | number | FanDuel player identifier. |
| `firstName` | string | Player first name. |
| `globalTeamID` | number | Global team identifier. |
| `height` | number | Player height in inches. |
| `jersey` | number | Jersey number. |
| `lastName` | string | Player last name. |
| `nbaDotComPlayerID` | number | NBA.com player identifier. |
| `photoUrl` | string | Provider photo URL. |
| `playerID` | number | SportsData player identifier. |
| `position` | string | Roster position. |
| `positionCategory` | string | Broad position group. |
| `salary` | number | Salary when available. |
| `sportRadarPlayerID` | string | SportRadar player identifier. |
| `status` | string | Roster status. |
| `team` | string | Team abbreviation. |
| `teamID` | number | Team identifier. |
| `usaTodayHeadshotNoBackgroundUrl` | string | USA Today transparent headshot URL. |
| `usaTodayHeadshotUrl` | string | USA Today headshot URL. |
| `weight` | number | Player weight. |
| `yahooName` | string | Yahoo display name. |
| `yahooPlayerID` | number | Yahoo player identifier. |

## Native endpoint

Through the native SportsData API, this operation is `GET /v3/nba/scores/json/Players` (base URL `https://api.sportsdata.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nba-players.md) for the provider-specific parameters and requirements.


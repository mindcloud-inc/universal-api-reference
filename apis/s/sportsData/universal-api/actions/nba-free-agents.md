# SportsData: NBA Free Agents

Retrieves NBA free agents from SportsData.

```
GET https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-free-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SportsData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-free-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-free-agents?${params}`, {
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
      "firstName": "Ava",
      "globalTeamID": 1,
      "height": 1,
      "jersey": 1,
      "lastName": "Chen",
      "playerID": 1,
      "position": "string",
      "positionCategory": "string",
      "sportsDataID": "string",
      "status": "string",
      "team": "string",
      "teamID": 1,
      "weight": 1
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
| `firstName` | string | Player first name. |
| `globalTeamID` | number | Global team identifier. |
| `height` | number | Player height in inches. |
| `jersey` | number | Jersey number when assigned. |
| `lastName` | string | Player last name. |
| `playerID` | number | SportsData player identifier. |
| `position` | string | Roster position. |
| `positionCategory` | string | Broad position group. |
| `sportsDataID` | string | Provider SportsData string identifier. |
| `status` | string | Roster status. |
| `team` | string | Team abbreviation when assigned. |
| `teamID` | number | Team identifier when assigned. |
| `weight` | number | Player weight. |

## Native endpoint

Through the native SportsData API, this operation is `GET /v3/nba/scores/json/PlayersByFreeAgents` (base URL `https://api.sportsdata.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nba-free-agents.md) for the provider-specific parameters and requirements.


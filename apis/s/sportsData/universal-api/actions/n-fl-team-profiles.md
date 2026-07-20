# SportsData: NFL Team Profiles

Retrieves active NFL team profiles from SportsData.

```
GET https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/n-fl-team-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SportsData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/n-fl-team-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/n-fl-team-profiles?${params}`, {
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
      "averageDraftPosition": 1,
      "averageDraftPosition2QB": 1,
      "averageDraftPositionDynasty": 1,
      "averageDraftPositionPPR": 1,
      "byeWeek": 1,
      "city": "string",
      "conference": "string",
      "defensiveCoordinator": "string",
      "defensiveScheme": "string",
      "division": "string",
      "draftKingsName": "Ava Chen",
      "draftKingsPlayerID": 1,
      "fanDuelName": "Ava Chen",
      "fanDuelPlayerID": 1,
      "fantasyDraftName": "Ava Chen",
      "fantasyDraftPlayerID": 1,
      "fullName": "Ava Chen",
      "globalTeamID": 1,
      "headCoach": "string",
      "key": "string",
      "name": "Ava Chen",
      "offensiveCoordinator": "string",
      "offensiveScheme": "string",
      "playerID": 1,
      "primaryColor": "string",
      "quaternaryColor": "string",
      "secondaryColor": "string",
      "specialTeamsCoach": "string",
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
      "teamID": 1,
      "tertiaryColor": "string",
      "upcomingDraftKingsSalary": 1,
      "upcomingFanDuelSalary": 1,
      "upcomingOpponent": "string",
      "upcomingOpponentPositionRank": 1,
      "upcomingOpponentRank": 1,
      "upcomingSalary": 1,
      "upcomingYahooSalary": 1,
      "wikipediaLogoUrl": "https://example.com",
      "wikipediaWordMarkUrl": "https://example.com",
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
| `averageDraftPosition` | number |  |
| `averageDraftPosition2QB` | number |  |
| `averageDraftPositionDynasty` | number |  |
| `averageDraftPositionPPR` | number |  |
| `byeWeek` | number |  |
| `city` | string |  |
| `conference` | string |  |
| `defensiveCoordinator` | string |  |
| `defensiveScheme` | string |  |
| `division` | string |  |
| `draftKingsName` | string |  |
| `draftKingsPlayerID` | number |  |
| `fanDuelName` | string |  |
| `fanDuelPlayerID` | number |  |
| `fantasyDraftName` | string |  |
| `fantasyDraftPlayerID` | number |  |
| `fullName` | string |  |
| `globalTeamID` | number |  |
| `headCoach` | string |  |
| `key` | string |  |
| `name` | string |  |
| `offensiveCoordinator` | string |  |
| `offensiveScheme` | string |  |
| `playerID` | number |  |
| `primaryColor` | string |  |
| `quaternaryColor` | string |  |
| `secondaryColor` | string |  |
| `specialTeamsCoach` | string |  |
| `stadiumDetails.capacity` | number |  |
| `stadiumDetails.city` | string |  |
| `stadiumDetails.country` | string |  |
| `stadiumDetails.geoLat` | number |  |
| `stadiumDetails.geoLong` | number |  |
| `stadiumDetails.name` | string |  |
| `stadiumDetails.playingSurface` | string |  |
| `stadiumDetails.stadiumID` | number |  |
| `stadiumDetails.state` | string |  |
| `stadiumDetails.type` | string |  |
| `stadiumID` | number |  |
| `teamID` | number |  |
| `tertiaryColor` | string |  |
| `upcomingDraftKingsSalary` | number |  |
| `upcomingFanDuelSalary` | number |  |
| `upcomingOpponent` | string |  |
| `upcomingOpponentPositionRank` | number |  |
| `upcomingOpponentRank` | number |  |
| `upcomingSalary` | number |  |
| `upcomingYahooSalary` | number |  |
| `wikipediaLogoUrl` | string |  |
| `wikipediaWordMarkUrl` | string |  |
| `yahooName` | string |  |
| `yahooPlayerID` | number |  |

## Native endpoint

Through the native SportsData API, this operation is `GET /v3/nfl/scores/json/Teams` (base URL `https://api.sportsdata.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/n-fl-team-profiles.md) for the provider-specific parameters and requirements.


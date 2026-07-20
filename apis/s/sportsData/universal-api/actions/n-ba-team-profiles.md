# SportsData: NBA Team Profiles

Retrieves active NBA team profiles from SportsData.

```
GET https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/n-ba-team-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SportsData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/n-ba-team-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/n-ba-team-profiles?${params}`, {
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
      "active": true,
      "city": "string",
      "conference": "string",
      "division": "string",
      "globalTeamID": 1,
      "headCoach": "string",
      "key": "string",
      "leagueID": 1,
      "name": "Ava Chen",
      "nbaDotComTeamID": 1,
      "primaryColor": "string",
      "quaternaryColor": "string",
      "secondaryColor": "string",
      "stadiumID": 1,
      "teamID": 1,
      "tertiaryColor": "string",
      "wikipediaLogoUrl": "https://example.com",
      "wikipediaWordMarkUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the team is active. |
| `city` | string | Team city. |
| `conference` | string | Conference name. |
| `division` | string | Division name. |
| `globalTeamID` | number | Global team identifier. |
| `headCoach` | string | Head coach name. |
| `key` | string | Team abbreviation. |
| `leagueID` | number | League identifier. |
| `name` | string | Team name. |
| `nbaDotComTeamID` | number | NBA.com team identifier. |
| `primaryColor` | string | Primary team color. |
| `quaternaryColor` | string | Quaternary team color. |
| `secondaryColor` | string | Secondary team color. |
| `stadiumID` | number | Home venue identifier. |
| `teamID` | number | SportsData team identifier. |
| `tertiaryColor` | string | Tertiary team color. |
| `wikipediaLogoUrl` | string | Wikipedia logo URL. |
| `wikipediaWordMarkUrl` | string | Wikipedia wordmark URL. |

## Native endpoint

Through the native SportsData API, this operation is `GET /v3/nba/scores/json/teams` (base URL `https://api.sportsdata.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/n-ba-team-profiles.md) for the provider-specific parameters and requirements.


# SportsData: NFL Free Agents

Retrieves NFL free agents from SportsData.

```
GET https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-free-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SportsData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-free-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-free-agents?${params}`, {
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
      "age": 1,
      "averageDraftPosition": 1,
      "birthDate": "2026-05-07T12:00:00.000Z",
      "birthDateString": "string",
      "byeWeek": 1,
      "college": "string",
      "collegeDraftPick": 1,
      "collegeDraftRound": 1,
      "collegeDraftTeam": "string",
      "collegeDraftYear": 1,
      "currentTeam": "string",
      "experience": 1,
      "experienceString": "string",
      "fantasyPosition": "string",
      "firstName": "Ava",
      "globalTeamID": 1,
      "height": "string",
      "heightFeet": 1,
      "heightInches": 1,
      "isUndraftedFreeAgent": true,
      "lastName": "Chen",
      "latestNews": [
        {}
      ],
      "name": "Ava Chen",
      "number": 1,
      "photoUrl": "https://example.com",
      "playerID": 1,
      "position": "string",
      "positionCategory": "string",
      "shortName": "Ava Chen",
      "status": "string",
      "team": "string",
      "teamID": 1,
      "usaTodayHeadshotNoBackgroundUrl": "https://example.com",
      "usaTodayHeadshotUrl": "https://example.com",
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the player is active. |
| `age` | number | Player age. |
| `averageDraftPosition` | number | Average draft position. |
| `birthDate` | date | Player birth date. |
| `birthDateString` | string | Human-readable birth date. |
| `byeWeek` | number | Bye week. |
| `college` | string | Player college. |
| `collegeDraftPick` | number | Draft pick number. |
| `collegeDraftRound` | number | Draft round. |
| `collegeDraftTeam` | string | Drafting team abbreviation. |
| `collegeDraftYear` | number | Draft year. |
| `currentTeam` | string | Current team abbreviation. |
| `experience` | number | SportsData experience code. |
| `experienceString` | string | Human-readable experience label. |
| `fantasyPosition` | string | Fantasy position. |
| `firstName` | string | Player first name. |
| `globalTeamID` | number | Global team identifier. |
| `height` | string | Player height text. |
| `heightFeet` | number | Height in feet. |
| `heightInches` | number | Remaining height inches. |
| `isUndraftedFreeAgent` | boolean | Whether the player entered the league as an undrafted free agent. |
| `lastName` | string | Player last name. |
| `latestNews` | array<object> | Latest linked news items for the player. |
| `name` | string | Full player name. |
| `number` | number | Jersey number. |
| `photoUrl` | string | Player photo URL. |
| `playerID` | number | SportsData player identifier. |
| `position` | string | Roster position. |
| `positionCategory` | string | Offense or defense category. |
| `shortName` | string | Short display name. |
| `status` | string | Roster status. |
| `team` | string | Team abbreviation. |
| `teamID` | number | Team identifier. |
| `usaTodayHeadshotNoBackgroundUrl` | string | USA Today transparent headshot URL. |
| `usaTodayHeadshotUrl` | string | USA Today headshot URL. |
| `weight` | number | Player weight. |

## Native endpoint

Through the native SportsData API, this operation is `GET /v3/nfl/scores/json/FreeAgents` (base URL `https://api.sportsdata.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nfl-free-agents.md) for the provider-specific parameters and requirements.


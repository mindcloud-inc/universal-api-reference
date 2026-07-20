# College Football Data: List Game Havoc Stats

Retrieves game havoc statistics from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-game-havoc-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-game-havoc-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-game-havoc-stats?${params}`, {
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
| `year` | number | no | Year filter, required if team not specified |
| `team` | string | no | Team filter, required if year not specified |
| `week` | number | no | Optional week filter |
| `opponent` | string | no | Optional opponent filter |
| `seasonType` | string | no | Optional season type filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conference": "string",
      "defense": {
        "dbHavocEvents": 1,
        "dbHavocRate": 1,
        "frontSevenHavocEvents": 1,
        "frontSevenHavocRate": 1,
        "havocRate": 1,
        "totalHavocEvents": 1,
        "totalPlays": 1
      },
      "gameId": 1,
      "offense": {
        "dbHavocEvents": 1,
        "dbHavocRate": 1,
        "frontSevenHavocEvents": 1,
        "frontSevenHavocRate": 1,
        "havocRate": 1,
        "totalHavocEvents": 1,
        "totalPlays": 1
      },
      "opponent": "string",
      "opponentConference": "string",
      "season": 1,
      "seasonType": "string",
      "team": "string",
      "week": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conference` | string |  |
| `defense.dbHavocEvents` | number |  |
| `defense.dbHavocRate` | number |  |
| `defense.frontSevenHavocEvents` | number |  |
| `defense.frontSevenHavocRate` | number |  |
| `defense.havocRate` | number |  |
| `defense.totalHavocEvents` | number |  |
| `defense.totalPlays` | number |  |
| `gameId` | number |  |
| `offense.dbHavocEvents` | number |  |
| `offense.dbHavocRate` | number |  |
| `offense.frontSevenHavocEvents` | number |  |
| `offense.frontSevenHavocRate` | number |  |
| `offense.havocRate` | number |  |
| `offense.totalHavocEvents` | number |  |
| `offense.totalPlays` | number |  |
| `opponent` | string |  |
| `opponentConference` | string |  |
| `season` | number |  |
| `seasonType` | string |  |
| `team` | string |  |
| `week` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /stats/game/havoc` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-game-havoc-stats.md) for the provider-specific parameters and requirements.


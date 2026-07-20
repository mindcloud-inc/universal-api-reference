# College Football Data: List Predicted Points Added By Game

Retrieves team PPA metrics by game from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-predicted-points-added-by-game
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-predicted-points-added-by-game?connectionId=$CONNECTION_ID&year=2025" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2025"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-predicted-points-added-by-game?${params}`, {
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
| `year` | number | yes | Required year filter Default: `2025`. |
| `week` | number | no | Optional week filter |
| `seasonType` | string | no | Optional season type filter |
| `team` | string | no | Optional team filter |
| `conference` | string | no | Optional conference abbreviation filter |
| `excludeGarbageTime` | boolean | no | Optional flag to exclude garbage time plays |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conference": "string",
      "defense": {
        "firstDown": 1,
        "overall": 1,
        "passing": 1,
        "rushing": 1,
        "secondDown": 1,
        "thirdDown": 1
      },
      "gameId": 1,
      "offense": {
        "firstDown": 1,
        "overall": 1,
        "passing": 1,
        "rushing": 1,
        "secondDown": 1,
        "thirdDown": 1
      },
      "opponent": "string",
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
| `defense.firstDown` | number |  |
| `defense.overall` | number |  |
| `defense.passing` | number |  |
| `defense.rushing` | number |  |
| `defense.secondDown` | number |  |
| `defense.thirdDown` | number |  |
| `gameId` | number |  |
| `offense.firstDown` | number |  |
| `offense.overall` | number |  |
| `offense.passing` | number |  |
| `offense.rushing` | number |  |
| `offense.secondDown` | number |  |
| `offense.thirdDown` | number |  |
| `opponent` | string |  |
| `season` | number |  |
| `seasonType` | string |  |
| `team` | string |  |
| `week` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /ppa/games` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-predicted-points-added-by-game.md) for the provider-specific parameters and requirements.


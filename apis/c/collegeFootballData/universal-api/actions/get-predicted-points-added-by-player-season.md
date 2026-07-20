# College Football Data: List Predicted Points Added By Player Season

Retrieves player PPA statistics by season from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-predicted-points-added-by-player-season
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-predicted-points-added-by-player-season?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-predicted-points-added-by-player-season?${params}`, {
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
| `year` | number | no | Year filter, required if playerId not specified |
| `conference` | string | no | Optional conference abbreviation filter |
| `team` | string | no | Optional team filter |
| `position` | string | no | Optional position abbreviation filter |
| `playerId` | string | no | Player ID filter, required if year not specified |
| `threshold` | number | no | Threshold value for minimum number of plays |
| `excludeGarbageTime` | boolean | no | Optional flag to exclude garbage time plays |

## Response

```json
{
  "success": true,
  "data": [
    {
      "averagePPA": {
        "all": 1,
        "firstDown": 1,
        "pass": 1,
        "passingDowns": 1,
        "rush": 1,
        "secondDown": 1,
        "standardDowns": 1,
        "thirdDown": 1
      },
      "conference": "string",
      "id": "string",
      "name": "Ava Chen",
      "position": "string",
      "season": 1,
      "team": "string",
      "totalPPA": {
        "all": 1,
        "firstDown": 1,
        "pass": 1,
        "passingDowns": 1,
        "rush": 1,
        "secondDown": 1,
        "standardDowns": 1,
        "thirdDown": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averagePPA.all` | number |  |
| `averagePPA.firstDown` | number |  |
| `averagePPA.pass` | number |  |
| `averagePPA.passingDowns` | number |  |
| `averagePPA.rush` | number |  |
| `averagePPA.secondDown` | number |  |
| `averagePPA.standardDowns` | number |  |
| `averagePPA.thirdDown` | number |  |
| `conference` | string |  |
| `id` | string |  |
| `name` | string |  |
| `position` | string |  |
| `season` | number |  |
| `team` | string |  |
| `totalPPA.all` | number |  |
| `totalPPA.firstDown` | number |  |
| `totalPPA.pass` | number |  |
| `totalPPA.passingDowns` | number |  |
| `totalPPA.rush` | number |  |
| `totalPPA.secondDown` | number |  |
| `totalPPA.standardDowns` | number |  |
| `totalPPA.thirdDown` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /ppa/players/season` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-predicted-points-added-by-player-season.md) for the provider-specific parameters and requirements.


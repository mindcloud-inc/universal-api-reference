# College Football Data: List Player Usage

Retrieves player usage data from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-player-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-player-usage?connectionId=$CONNECTION_ID&year=2025" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2025"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-player-usage?${params}`, {
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
| `conference` | string | no | Optional conference abbreviation filter |
| `position` | string | no | Optional position abbreivation filter |
| `team` | string | no | Optional team filter |
| `playerId` | number | no | Optional player id filter |
| `excludeGarbageTime` | boolean | no | Optional exclude garbage time flag, defaults to false |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conference": "string",
      "id": "string",
      "name": "Ava Chen",
      "position": "string",
      "season": 1,
      "team": "string",
      "usage": {
        "firstDown": 1,
        "overall": 1,
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
| `conference` | string |  |
| `id` | string |  |
| `name` | string |  |
| `position` | string |  |
| `season` | number |  |
| `team` | string |  |
| `usage.firstDown` | number |  |
| `usage.overall` | number |  |
| `usage.pass` | number |  |
| `usage.passingDowns` | number |  |
| `usage.rush` | number |  |
| `usage.secondDown` | number |  |
| `usage.standardDowns` | number |  |
| `usage.thirdDown` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /player/usage` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-player-usage.md) for the provider-specific parameters and requirements.


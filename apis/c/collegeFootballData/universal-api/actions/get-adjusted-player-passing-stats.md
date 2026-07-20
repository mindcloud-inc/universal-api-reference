# College Football Data: List Adjusted Player Passing Stats

Retrieves opponent-adjusted player passing statistics from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-adjusted-player-passing-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-adjusted-player-passing-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-adjusted-player-passing-stats?${params}`, {
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
| `year` | number | no | Optional year filter |
| `team` | string | no | Optional team filter |
| `conference` | string | no | Optional conference abbreviation filter |
| `position` | string | no | Optional position abbreviation filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "athleteId": "string",
      "athleteName": "Ava Chen",
      "conference": "string",
      "plays": 1,
      "position": "string",
      "team": "string",
      "wepa": 1,
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `athleteId` | string |  |
| `athleteName` | string |  |
| `conference` | string |  |
| `plays` | number |  |
| `position` | string |  |
| `team` | string |  |
| `wepa` | number |  |
| `year` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /wepa/players/passing` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-adjusted-player-passing-stats.md) for the provider-specific parameters and requirements.


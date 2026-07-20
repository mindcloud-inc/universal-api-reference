# College Football Data: List Team Stats

Retrieves team season statistics from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-team-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-team-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-team-stats?${params}`, {
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
| `conference` | string | no | Optional conference filter |
| `startWeek` | number | no | Optional week start range filter |
| `endWeek` | number | no | Optional week end range filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conference": "string",
      "season": 1,
      "statName": "Ava Chen",
      "statValue": "string",
      "team": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conference` | string |  |
| `season` | number |  |
| `statName` | string |  |
| `statValue` | string |  |
| `team` | string |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /stats/season` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-stats.md) for the provider-specific parameters and requirements.


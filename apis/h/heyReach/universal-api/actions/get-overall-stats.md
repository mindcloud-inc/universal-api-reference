# Hey Reach: Get Overall Stats

Retrieves overall stats from Hey Reach.

```
GET https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-overall-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-overall-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-overall-stats?${params}`, {
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
| `accountIds[]` | array<number> | no |  |
| `campaignIds[]` | array<string> | no |  |
| `startDate` | date | no |  |
| `endDate` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "byDayStats": {},
      "overallStats": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `byDayStats` | object |  |
| `overallStats` | object |  |

## Native endpoint

Through the native Hey Reach API, this operation is `POST /api/public/stats/GetOverallStats` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-overall-stats.md) for the provider-specific parameters and requirements.


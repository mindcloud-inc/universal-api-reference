# CallScaler: Get Call Analytics

Retrieves call analytics from CallScaler.

```
GET https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/get-call-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallScaler `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/get-call-analytics?connectionId=$CONNECTION_ID&groupBy=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupBy": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/get-call-analytics?${params}`, {
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
| `callFlowId` | string | no |  |
| `direction` | string | no |  |
| `endDate` | date | no |  |
| `groupBy` | string | yes |  |
| `metrics` | string | no | Accepts multiple values in one string, delimited by `,`. |
| `numberId` | string | no |  |
| `qualified` | boolean | no |  |
| `source` | string | no |  |
| `startDate` | date | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "avg_ai_score": 1,
          "count": 1,
          "qualified_pct": 1,
          "source": "string"
        }
      ],
      "totals": {
        "avg_ai_score": 1,
        "count": 1,
        "qualified_pct": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of analytics groups returned. |
| `data` | array<object> | Grouped analytics result rows. |
| `data[].avg_ai_score` | number | Average AI score metric for a group. |
| `data[].count` | number | Count metric for a group. |
| `data[].qualified_pct` | number | Qualified percentage metric for a group. |
| `data[].source` | string | Example grouped source value. |
| `totals` | object | Totals across all matching calls. |
| `totals.avg_ai_score` | number | Average AI score across matching calls. |
| `totals.count` | number | Total count across matching calls. |
| `totals.qualified_pct` | number | Qualified percentage across matching calls. |

## Native endpoint

Through the native CallScaler API, this operation is `GET /analytics/calls` (base URL `https://callscaler.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-analytics.md) for the provider-specific parameters and requirements.


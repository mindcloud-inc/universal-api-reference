# ProfitWell: Get Daily Metrics

Retrieves daily metrics from ProfitWell.

```
GET https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/get-daily-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/get-daily-metrics?connectionId=$CONNECTION_ID&month=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "month": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/get-daily-metrics?${params}`, {
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
| `month` | string | yes | Return daily metrics trends for this month in YYYY-MM format. Can only be the current or previous month. |
| `planId` | string | no | Optionally only return the metrics for this plan ID. |
| `metrics` | string | no | Optional comma-separated list of metrics trends to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Metrics trend data keyed by metric name, where each value is an array of {date, value} records. |

## Native endpoint

Through the native ProfitWell API, this operation is `GET /v2/metrics/daily` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-daily-metrics.md) for the provider-specific parameters and requirements.


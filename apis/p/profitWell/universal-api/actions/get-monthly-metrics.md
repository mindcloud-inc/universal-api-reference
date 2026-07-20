# ProfitWell: Get Monthly Metrics

Retrieves monthly metrics from ProfitWell.

```
GET https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/get-monthly-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/get-monthly-metrics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/get-monthly-metrics?${params}`, {
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

Through the native ProfitWell API, this operation is `GET /v2/metrics/monthly` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-monthly-metrics.md) for the provider-specific parameters and requirements.


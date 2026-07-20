# Quantcast: Get Available Breakdowns And Metrics

Retrieves available breakdowns and metrics from Quantcast.

```
GET https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/get-available-breakdowns-and-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/get-available-breakdowns-and-metrics?connectionId=$CONNECTION_ID&accountId=9974296" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "9974296"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantcast/latest/actions/get-available-breakdowns-and-metrics?${params}`, {
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
| `accountId` | number | yes | Quantcast account ID to inspect. Default: `9974296`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableBreakdownsAndMetrics": {
        "breakdowns": {
          "name": "Ava Chen"
        },
        "metrics": {
          "name": "Ava Chen"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableBreakdownsAndMetrics` | object | Breakdown and metric options available for a Quantcast account. |
| `availableBreakdownsAndMetrics.breakdowns` | array<object> | Available breakdown definitions. |
| `availableBreakdownsAndMetrics.breakdowns.name` | string | Breakdown display name. |
| `availableBreakdownsAndMetrics.metrics` | array<object> | Available metric definitions. |
| `availableBreakdownsAndMetrics.metrics.name` | string | Metric display name. |

## Native endpoint

Through the native Quantcast API, this operation is `GET /api/v2/graphql` (base URL `https://developers.quantcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-available-breakdowns-and-metrics.md) for the provider-specific parameters and requirements.


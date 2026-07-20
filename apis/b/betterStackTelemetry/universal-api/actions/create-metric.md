# Better Stack Telemetry: Create Metric

Creates a new metric in Better Stack Telemetry.

```
POST https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/create-metric
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Telemetry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/create-metric" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceId": "string",
  "name": "Ava Chen",
  "sqlExpression": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/create-metric', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceId": "string",
    "name": "Ava Chen",
    "sqlExpression": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | string | yes | Source for which to create a metric |
| `name` | string | yes | Metric name |
| `sqlExpression` | string | yes | SQL expression to use for the metric |
| `teamName` | string | no | Required if using a global API token to specify the team that should own the metric |
| `aggregations[]` | array<string> | no | Aggregations to apply to the metric |
| `type` | string | no | Metric type |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Telemetry API returns.

## Native endpoint

Through the native Better Stack Telemetry API, this operation is `POST /api/v2/sources/:source_id/metrics` (base URL `https://telemetry.betterstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-metric.md) for the provider-specific parameters and requirements.


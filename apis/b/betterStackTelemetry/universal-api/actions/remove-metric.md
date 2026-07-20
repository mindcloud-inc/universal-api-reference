# Better Stack Telemetry: Remove Metric

Deletes an existing metric from Better Stack Telemetry.

```
DELETE https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/remove-metric
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Telemetry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/remove-metric?connectionId=$CONNECTION_ID&sourceId=string&metricId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceId": "string",
  "metricId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/remove-metric?${params}`, {
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
| `sourceId` | string | yes | Source for which to delete a metric |
| `metricId` | string | yes | ID of the metric to delete |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Telemetry API returns.

## Native endpoint

Through the native Better Stack Telemetry API, this operation is `DELETE /api/v2/sources/:source_id/metrics/:id` (base URL `https://telemetry.betterstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-metric.md) for the provider-specific parameters and requirements.


# Statsig: Create Metric

Creates a metric in Statsig.

```
POST https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-metric-post-console-v1-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-metric-post-console-v1-metrics" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-metric-post-console-v1-metrics', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Request body field. |
| `type` | string | yes | Request body field. |
| `isVerified` | boolean | no | Request body field. |
| `isReadOnly` | boolean | no | Request body field. |
| `unitTypes` | list | no | Request body field. |
| `metricEvents` | list | no | Request body field. |
| `metricComponentMetrics` | list | no | Request body field. |
| `description` | string | no | Request body field. |
| `directionality` | string | no | Request body field. |
| `tags` | string | no | Request body field. |
| `isPermanent` | boolean | no | Request body field. |
| `rollupTimeWindow` | string | no | Request body field. |
| `customRollUpStart` | number | no | Request body field. |
| `customRollUpEnd` | number | no | Request body field. |
| `funnelEventList` | list | no | Request body field. |
| `funnelCountDistinct` | string | no | Request body field. |
| `warehouseNative` | object | no | Request body field. |
| `team` | string | no | Request body field. |
| `teamID` | string | no | Request body field. |
| `dryRun` | boolean | no | Request body field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `POST /console/v1/metrics` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-metric-post-console-v1-metrics.md) for the provider-specific parameters and requirements.


# Better Stack Telemetry: Create Exploration Alert

Creates a new exploration alert in Better Stack Telemetry.

```
POST https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/create-exploration-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Telemetry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/create-exploration-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "explorationId": "746510",
  "name": "mc-stage3-alert-paused",
  "alertType": "threshold",
  "confirmationPeriod": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/create-exploration-alert', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "explorationId": "746510",
    "name": "mc-stage3-alert-paused",
    "alertType": "threshold",
    "confirmationPeriod": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `explorationId` | string | yes | The ID of the exploration to add the alert to. Example: `746510`. |
| `name` | string | yes | The name of the alert. Example: `mc-stage3-alert-paused`. |
| `alertType` | string | yes | The type of alert. Example: `threshold`. |
| `operator` | string | no | Comparison operator for threshold and relative alerts. Example: `higher_than`. |
| `value` | number | no | Numeric value for the alert condition. Example: `100`. |
| `confirmationPeriod` | number | yes | Seconds the condition must hold before alerting. Default: `0`. Example: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stringValue` | string | no | Exact string match value for threshold alerts. Example: `ERROR`. |
| `anomalySensitivity` | number | no | Sensitivity for anomaly alerts. Example: `75`. |
| `anomalyTrigger` | string | no | Which anomalies trigger the alert. Example: `higher`. |
| `queryPeriod` | number | no | Time window in seconds for analyzed data. Example: `300`. |
| `recoveryPeriod` | number | no | Seconds the condition must be resolved before recovery. Example: `300`. |
| `checkPeriod` | number | no | How often to evaluate threshold and relative alerts. Example: `300`. |
| `aggregationInterval` | number | no | Aggregation interval in seconds. Example: `60`. |
| `seriesNames[]` | array | no | Series names to scope the alert to. |
| `sourceVariable` | string | no | Source variable used for source selection. Example: `source`. |
| `sourceMode` | string | no | Mode for source selection. Example: `source_variable`. |
| `sourcePlatforms[]` | array | no | Platforms used for source selection. |
| `incidentCause` | string | no | Cause text included in incidents. Example: `Stage 3 paused verification alert`. |
| `incidentPerSeries` | boolean | no | Create a separate incident for each triggering series. |
| `escalationTarget` | object | no | Notification target object. Example: `[object Object]`. |
| `call` | boolean | no | Enable phone call notifications. |
| `sms` | boolean | no | Enable SMS notifications. |
| `email` | boolean | no | Enable email notifications. |
| `push` | boolean | no | Enable push notifications. |
| `criticalAlert` | boolean | no | Enable critical push notifications. |
| `metadata` | object | no | Custom metadata object. |
| `paused` | boolean | no | Create the alert in a paused state. Default: `true`. |
| `teamName` | string | no | Team name for global API tokens. Example: `Your team`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Telemetry API returns.

## Native endpoint

Through the native Better Stack Telemetry API, this operation is `POST /api/v2/explorations/:exploration_id/alerts` (base URL `https://telemetry.betterstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-exploration-alert.md) for the provider-specific parameters and requirements.


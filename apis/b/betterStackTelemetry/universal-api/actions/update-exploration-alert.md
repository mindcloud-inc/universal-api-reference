# Better Stack Telemetry: Update Exploration Alert

Updates an existing exploration alert in Better Stack Telemetry.

```
PUT https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/update-exploration-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Telemetry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/update-exploration-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "explorationId": "746510",
  "id": "1857617807"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/update-exploration-alert', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "explorationId": "746510",
    "id": "1857617807"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `explorationId` | string | yes | The ID of the exploration that owns the alert. Example: `746510`. |
| `id` | string | yes | The ID of the alert to update. Example: `1857617807`. |
| `name` | string | no | Updated alert name. Example: `mc-stage3-alert-paused-updated`. |
| `confirmationPeriod` | number | no | Updated confirmation period in seconds. Example: `0`. |
| `paused` | boolean | no | Updated paused state. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `value` | number | no | Updated numeric value for the alert condition. Example: `999999`. |
| `stringValue` | string | no | Updated exact string match value. Example: `ERROR`. |
| `anomalySensitivity` | number | no | Updated anomaly sensitivity. Example: `75`. |
| `escalationTarget` | object | no | Updated notification target object. Example: `[object Object]`. |
| `metadata` | object | no | Updated custom metadata object. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Telemetry API returns.

## Native endpoint

Through the native Better Stack Telemetry API, this operation is `PATCH /api/v2/explorations/:exploration_id/alerts/:id` (base URL `https://telemetry.betterstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-exploration-alert.md) for the provider-specific parameters and requirements.


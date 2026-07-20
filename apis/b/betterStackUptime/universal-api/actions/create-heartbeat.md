# Better Stack Uptime: Create Heartbeat

Creates a new heartbeat in Better Stack Uptime.

```
POST https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/create-heartbeat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Uptime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/create-heartbeat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "period": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/create-heartbeat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "period": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The heartbeat name. |
| `period` | number | yes | The expected heartbeat period in seconds. |
| `grace` | number | no | The grace period in seconds. |
| `email` | boolean | no | Whether email alerts are enabled. |
| `sms` | boolean | no | Whether SMS alerts are enabled. |
| `call` | boolean | no | Whether call alerts are enabled. |
| `push` | boolean | no | Whether push alerts are enabled. |
| `criticalAlert` | boolean | no | Whether critical alerts are enabled. |
| `teamWait` | boolean | no | Whether team wait is enabled. |
| `paused` | boolean | no | Whether the heartbeat is paused. |
| `sortIndex` | number | no | The sort index. |
| `maintenanceDays[]` | array<string> | no | Maintenance days. |
| `maintenanceFrom` | string | no | Maintenance window start time. |
| `maintenanceTo` | string | no | Maintenance window end time. |
| `maintenanceTimezone` | string | no | Maintenance timezone. |
| `heartbeatGroupId` | number | no | The heartbeat group ID. |
| `policyId` | number | no | The escalation policy ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Uptime API returns.

## Native endpoint

Through the native Better Stack Uptime API, this operation is `POST /v2/heartbeats` (base URL `https://uptime.betterstack.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-heartbeat.md) for the provider-specific parameters and requirements.


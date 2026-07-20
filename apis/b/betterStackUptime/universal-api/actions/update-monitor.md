# Better Stack Uptime: Update Monitor

Updates an existing monitor in Better Stack Uptime.

```
PUT https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/update-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Uptime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/update-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "monitorId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/update-monitor', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "monitorId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `monitorId` | string | yes | The ID of the monitor you want to update |
| `pronounceableName` | string | no | The name of the monitor |
| `email` | boolean | no | Send email alerts |
| `sms` | boolean | no | Send SMS alerts |
| `call` | boolean | no | Phone call alerts |
| `push` | boolean | no | Should we send a push notification to the on-call person? |
| `criticalAlert` | boolean | no | Send a critical alert to the on-call person |
| `checkFrequency` | number | no | Check frequency in seconds |
| `paused` | boolean | no | Set to true to pause monitoring |
| `verifySsl` | boolean | no | Whether to verify SSL certificates |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Uptime API returns.

## Native endpoint

Through the native Better Stack Uptime API, this operation is `PATCH /v2/monitors/:monitor_id` (base URL `https://uptime.betterstack.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-monitor.md) for the provider-specific parameters and requirements.


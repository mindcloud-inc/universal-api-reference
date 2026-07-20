# Better Stack Uptime: Create Monitor

Creates a new monitor in Better Stack Uptime.

```
POST https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/create-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Uptime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/create-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "monitorType": "string",
  "url": "https://example.com",
  "pronounceableName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/create-monitor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "monitorType": "string",
    "url": "https://example.com",
    "pronounceableName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `monitorType` | string | yes | Valid monitor type from Better Stack, such as status or expected_status_code |
| `url` | string | yes | The URL of your website or the host you want to ping |
| `pronounceableName` | string | yes | The name of the monitor |
| `email` | boolean | no | Send email alerts |
| `sms` | boolean | no | Send SMS alerts |
| `call` | boolean | no | Phone call alerts |
| `criticalAlert` | boolean | no | Send a critical alert to the on-call person |
| `checkFrequency` | number | no | Check frequency in seconds |
| `paused` | boolean | no | Set to true to pause monitoring |
| `verifySsl` | boolean | no | Whether to verify SSL certificates |
| `push` | boolean | no | Should we send a push notification to the on-call person? |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Uptime API returns.

## Native endpoint

Through the native Better Stack Uptime API, this operation is `POST /v2/monitors` (base URL `https://uptime.betterstack.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-monitor.md) for the provider-specific parameters and requirements.


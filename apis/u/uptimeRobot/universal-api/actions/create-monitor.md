# UptimeRobot: Create Monitor

Creates a new monitor in UptimeRobot.

```
POST https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/create-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UptimeRobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/create-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "friendly_name": "Ava Chen",
  "url": "https://example.com",
  "type": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/create-monitor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "friendly_name": "Ava Chen",
    "url": "https://example.com",
    "type": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `friendly_name` | string | yes | Monitor display name. |
| `url` | string | yes | Target URL or IP to monitor. |
| `type` | number | yes | Monitor type. Legacy docs: 1 HTTP(s), 2 keyword, 3 ping, 4 port, 5 heartbeat. |
| `interval` | number | no | Optional monitor interval in seconds. |
| `timeout` | number | no | Optional timeout in seconds for HTTP, keyword, and port monitors. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "monitor": {},
      "stat": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `monitor` | object |  |
| `stat` | string |  |

## Native endpoint

Through the native UptimeRobot API, this operation is `POST /newMonitor` (base URL `https://api.uptimerobot.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-monitor.md) for the provider-specific parameters and requirements.


# UptimeRobot: Reset Monitor

Resets an existing monitor's stats and response times in UptimeRobot.

```
PUT https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/reset-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UptimeRobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/reset-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/reset-monitor', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the monitor to reset. |

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

Through the native UptimeRobot API, this operation is `POST /resetMonitor` (base URL `https://api.uptimerobot.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reset-monitor.md) for the provider-specific parameters and requirements.


# UptimeRobot: Create Maintenance Window

Creates a new maintenance window in UptimeRobot.

```
POST https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/create-maintenance-window
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UptimeRobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/create-maintenance-window" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "friendly_name": "Ava Chen",
  "type": 1,
  "start_time": "string",
  "duration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/create-maintenance-window', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "friendly_name": "Ava Chen",
    "type": 1,
    "start_time": "string",
    "duration": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `friendly_name` | string | yes | Maintenance window display name. |
| `value` | string | no | Optional recurrence value for weekly or monthly windows, such as 2-4-5. |
| `type` | number | yes | Maintenance window type. Legacy docs: 1 once, 2 daily, 3 weekly, 4 monthly. |
| `start_time` | string | yes | Start time. Use Unix time for once windows or HH:mm for repeating windows. |
| `duration` | number | yes | Duration in minutes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mwindow": {},
      "stat": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mwindow` | object |  |
| `stat` | string |  |

## Native endpoint

Through the native UptimeRobot API, this operation is `POST /newMWindow` (base URL `https://api.uptimerobot.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-maintenance-window.md) for the provider-specific parameters and requirements.


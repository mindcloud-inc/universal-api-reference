# UptimeRobot: Delete Monitor

Deletes an existing monitor from UptimeRobot.

```
DELETE https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/delete-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UptimeRobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/delete-monitor?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/delete-monitor?${params}`, {
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
| `id` | number | yes | ID of the monitor to delete. |

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

Through the native UptimeRobot API, this operation is `POST /deleteMonitor` (base URL `https://api.uptimerobot.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-monitor.md) for the provider-specific parameters and requirements.


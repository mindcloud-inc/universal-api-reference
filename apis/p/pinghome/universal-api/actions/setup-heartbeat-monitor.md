# Pinghome: Setup Heartbeat Monitor

Creates a new heartbeat monitor in Pinghome.

```
POST https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/setup-heartbeat-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/setup-heartbeat-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "serviceId": "string",
  "name": "Ava Chen",
  "interval": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/setup-heartbeat-monitor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "serviceId": "string",
    "name": "Ava Chen",
    "interval": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `serviceId` | string | yes | The unique service ID associated with the heartbeat resource. |
| `name` | string | yes |  |
| `interval` | number | yes | The expected heartbeat check-in interval in seconds. |
| `enabled` | boolean | no | Whether the heartbeat monitor is enabled. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `POST /resource-cmd/v1/heartbeat` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/setup-heartbeat-monitor.md) for the provider-specific parameters and requirements.


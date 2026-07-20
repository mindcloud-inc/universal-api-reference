# Pinghome: Update Heartbeat Monitor

Updates an existing heartbeat monitor in Pinghome.

```
PUT https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-heartbeat-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-heartbeat-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen",
  "serviceId": "string",
  "interval": 1,
  "methods[]": [
    "string"
  ],
  "enabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-heartbeat-monitor', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen",
    "serviceId": "string",
    "interval": 1,
    "methods[]": ["string"],
    "enabled": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique ID of the heartbeat monitor. |
| `name` | string | yes | The name of the heartbeat resource. |
| `serviceId` | string | yes | The service associated with the heartbeat. |
| `interval` | number | yes | The heartbeat interval in seconds. |
| `methods[]` | array<string> | yes | The HTTP methods allowed for heartbeat check-ins. |
| `enabled` | boolean | yes | Whether the heartbeat monitor is enabled. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `PUT /resource-cmd/v1/heartbeat/:id` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-heartbeat-monitor.md) for the provider-specific parameters and requirements.


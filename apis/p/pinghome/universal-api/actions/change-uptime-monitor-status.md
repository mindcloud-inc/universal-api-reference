# Pinghome: Change Uptime Monitor Status

Updates uptime monitor status in Pinghome.

```
PUT https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/change-uptime-monitor-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/change-uptime-monitor-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "enabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/change-uptime-monitor-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "enabled": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique ID of the uptime monitor. |
| `enabled` | boolean | yes | Whether the monitor should be enabled. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `PUT /resource-cmd/v1/resource/:id/status` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-uptime-monitor-status.md) for the provider-specific parameters and requirements.


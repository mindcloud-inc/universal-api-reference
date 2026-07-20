# Cloud 66: Reboot Server

Reboots a server in your Cloud 66 account.

```
PUT https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/reboot-server
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud 66 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/reboot-server" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stackId": "string",
  "serverId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/reboot-server', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stackId": "string",
    "serverId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stackId` | string | yes | The stack UID |
| `serverId` | string | yes | The server UID |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloud 66 API returns.

## Native endpoint

Through the native Cloud 66 API, this operation is `POST /stacks/:stack_id/servers/:server_id/reboot` (base URL `https://app.cloud66.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reboot-server.md) for the provider-specific parameters and requirements.


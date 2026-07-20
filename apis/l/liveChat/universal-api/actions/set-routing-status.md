# LiveChat: Set Routing Status

Updates an agent routing status in LiveChat.

```
PUT https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/set-routing-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LiveChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/set-routing-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveChat/latest/actions/set-routing-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | yes | Routing status to apply. |
| `agentId` | string | no | The agent ID to update. Defaults to the requester when omitted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Official Text Platform Agent Chat API docs specify this mutation returns no response payload (200 OK). |

## Native endpoint

Through the native LiveChat API, this operation is `POST /set_routing_status` (base URL `https://api.livechatinc.com/v3.6/agent/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-routing-status.md) for the provider-specific parameters and requirements.


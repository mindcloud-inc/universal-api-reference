# Maildrip: Update sending node status



```
PUT https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/update-sending-node-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/update-sending-node-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "nodeId": "string",
  "userId": "string",
  "status": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/update-sending-node-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "nodeId": "string",
    "userId": "string",
    "status": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nodeId` | string | yes | Sending node UUID |
| `userId` | string | yes | MongoDB User ID |
| `status` | number | yes | New status (0=inactive, 1=active) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Sending node status updated successfully |

## Native endpoint

Through the native Maildrip API, this operation is `PATCH /api/v1/mumara/sending-nodes/{nodeId}/status` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sending-node-status.md) for the provider-specific parameters and requirements.


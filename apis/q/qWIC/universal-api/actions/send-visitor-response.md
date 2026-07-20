# QWIC: Send Visitor Response

Sends a visitor response to a QWIC conversation.

```
PUT https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/send-visitor-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QWIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/send-visitor-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversation_id": "string",
  "message": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/send-visitor-response', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversation_id": "string",
    "message": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversation_id` | string | yes | QWIC conversation ID. |
| `message` | object | yes | Visitor text response message object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native QWIC API, this operation is `POST /api/v1/conversation/:conversation_id/messages` (base URL `https://app.qwic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-visitor-response.md) for the provider-specific parameters and requirements.


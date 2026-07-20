# QWIC: Send Agent Response to Conversation

Sends an agent response to a QWIC conversation.

```
PUT https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/send-agent-response-to-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QWIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/send-agent-response-to-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversation_id": "string",
  "message": {},
  "user.by": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/send-agent-response-to-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversation_id": "string",
    "message": {},
    "user.by": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversation_id` | string | yes | Conversation ID from Start API Conversation or another conversation-creation action. |
| `message` | object | yes | Agent text response payload from the QWIC public API docs. |
| `user.by` | string | yes | Agent email sending the response, as shown in the QWIC public API docs. |

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

Through the native QWIC API, this operation is `POST /api/v1/conversation/:conversation_id/messages` (base URL `https://app.qwic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-agent-response-to-conversation.md) for the provider-specific parameters and requirements.


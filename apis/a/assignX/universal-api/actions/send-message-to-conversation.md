# AssignX: Send Message to Conversation

Sends a message in an AssignX conversation.

```
POST https://connect.mindcloud.co/v1/universal/assignX/latest/actions/send-message-to-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssignX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assignX/latest/actions/send-message-to-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assignX/latest/actions/send-message-to-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Conversation identifier from List Agent Conversations or Create New Conversation. |
| `message` | string | yes | Message text to send to the conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": [
        {
          "actionObject": {},
          "agent": "string",
          "conversationId": "string",
          "messageId": "string",
          "response": "string",
          "status": 1,
          "trace": "string"
        }
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response[].actionObject` | object |  |
| `response[].agent` | string |  |
| `response[].conversationId` | string |  |
| `response[].messageId` | string |  |
| `response[].response` | string |  |
| `response[].status` | number |  |
| `response[].trace` | string |  |
| `status` | number |  |

## Native endpoint

Through the native AssignX API, this operation is `POST conversations/:id/message` (base URL `https://api.agentx.so/api/v1/access/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message-to-conversation.md) for the provider-specific parameters and requirements.


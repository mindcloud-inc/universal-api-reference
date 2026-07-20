# Dify: Send Chat Message

Creates a chat message in Dify.

```
POST https://connect.mindcloud.co/v1/universal/dify/latest/actions/send-chat-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dify/latest/actions/send-chat-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "string",
  "inputs": {},
  "user": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dify/latest/actions/send-chat-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "string",
    "inputs": {},
    "user": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | User input or question content. |
| `inputs` | object | yes | App input variables as key/value pairs. |
| `responseMode` | string | no | Response mode: streaming or blocking. |
| `user` | string | yes | User identifier, unique within the application. |
| `conversationId` | string | no | Conversation ID to continue an existing conversation. |
| `files` | list<object> | no | Files for multimodal understanding. |
| `autoGenerateName` | boolean | no | Whether to auto-generate the conversation title. |
| `workflowId` | string | no | Published workflow version ID to execute. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "conversationId": "string",
      "createdAt": 1,
      "event": "string",
      "id": "string",
      "messageId": "string",
      "metadata": {},
      "mode": "string",
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string |  |
| `conversationId` | string |  |
| `createdAt` | number |  |
| `event` | string |  |
| `id` | string |  |
| `messageId` | string |  |
| `metadata` | object |  |
| `mode` | string |  |
| `taskId` | string |  |

## Native endpoint

Through the native Dify API, this operation is `POST /chat-messages` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-chat-message.md) for the provider-specific parameters and requirements.


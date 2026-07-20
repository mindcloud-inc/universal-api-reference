# ReplyCX: Send File Reply To Conversation



```
POST https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/send-file-reply-to-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReplyCX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/send-file-reply-to-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "user.by": "string",
  "message.file.path": "string",
  "message.file.size": 1,
  "message.file.type": "string",
  "message.file.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/replyCX/latest/actions/send-file-reply-to-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "user.by": "string",
    "message.file.path": "string",
    "message.file.size": 1,
    "message.file.type": "string",
    "message.file.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes |  |
| `user.by` | string | yes |  |
| `message.file.path` | string | yes |  |
| `message.file.size` | number | yes |  |
| `message.file.type` | string | yes |  |
| `message.file.name` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ReplyCX API returns.

## Native endpoint

Through the native ReplyCX API, this operation is `POST /api/v1/conversation/:conversation_id/messages` (base URL `https://api.reply.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-file-reply-to-conversation.md) for the provider-specific parameters and requirements.


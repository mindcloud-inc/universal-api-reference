# WotNot: Send Agent File Response

Creates an agent file message in WotNot.

```
POST https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/send-agent-file-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WotNot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/send-agent-file-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "message.file.path": "string",
  "message.file.size": 1,
  "message.file.type": "string",
  "message.file.name": "Ava Chen",
  "user.by": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/send-agent-file-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "message.file.path": "string",
    "message.file.size": 1,
    "message.file.type": "string",
    "message.file.name": "Ava Chen",
    "user.by": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | Conversation ID |
| `message.file.path` | string | yes | Public file URL |
| `message.file.size` | number | yes | File size in MB |
| `message.file.type` | string | yes | File MIME type |
| `message.file.name` | string | yes | Filename shown to the user |
| `user.by` | string | yes | Agent email sending the response |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WotNot API returns.

## Native endpoint

Through the native WotNot API, this operation is `POST /api/v1/conversation/:conversation_id/messages` (base URL `https://api.wotnot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-agent-file-response.md) for the provider-specific parameters and requirements.


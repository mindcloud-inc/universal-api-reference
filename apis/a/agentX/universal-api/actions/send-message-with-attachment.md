# AgentX: Send Message With Attachment

Sends a message with an attachment in AgentX.

```
POST https://connect.mindcloud.co/v1/universal/agentX/latest/actions/send-message-with-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AgentX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentX/latest/actions/send-message-with-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentX/latest/actions/send-message-with-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | Conversation Id |
| `file` | file | no | File to upload |
| `message` | string | no | Message to send |
| `context` | number | no | Context for the message |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AgentX API returns.

## Native endpoint

Through the native AgentX API, this operation is `POST /conversations/:id/attachment` (base URL `https://api.agentx.so/api/v1/access`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message-with-attachment.md) for the provider-specific parameters and requirements.


# Langbase: Update Thread Message



```
PUT https://connect.mindcloud.co/v1/universal/langbase/latest/actions/update-thread-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/update-thread-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "threadId": "string",
  "messageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langbase/latest/actions/update-thread-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "threadId": "string",
    "messageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threadId` | string | yes | Thread ID that owns the message. |
| `messageId` | string | yes | Message ID to update. |
| `content` | string | no | Updated message content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "chatId": "string",
      "content": "string",
      "contentInKv": "string",
      "createdAt": "string",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "ownerOrgId": "string",
      "ownerUserId": "string",
      "pipeId": "string",
      "role": "string",
      "toolCallId": "string",
      "toolCalls": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `chatId` | string |  |
| `content` | string |  |
| `contentInKv` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `ownerOrgId` | string |  |
| `ownerUserId` | string |  |
| `pipeId` | string |  |
| `role` | string |  |
| `toolCallId` | string |  |
| `toolCalls` | array<object> |  |

## Native endpoint

Through the native Langbase API, this operation is `POST v1/threads/:threadId/messages/:messageId` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-thread-message.md) for the provider-specific parameters and requirements.


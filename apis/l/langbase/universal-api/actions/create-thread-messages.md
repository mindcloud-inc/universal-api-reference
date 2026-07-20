# Langbase: Create Thread Messages



```
POST https://connect.mindcloud.co/v1/universal/langbase/latest/actions/create-thread-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/create-thread-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "threadId": "string",
  "messages[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langbase/latest/actions/create-thread-messages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "threadId": "string",
    "messages[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threadId` | string | yes | Thread ID that will receive the new messages. |
| `messages[]` | array<object> | yes | Array of thread message objects to append. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "content": "string",
      "createdAt": 1,
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "role": "string",
      "threadId": "string",
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
| `content` | string |  |
| `createdAt` | number |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `role` | string |  |
| `threadId` | string |  |
| `toolCallId` | string |  |
| `toolCalls` | array<object> |  |

## Native endpoint

Through the native Langbase API, this operation is `POST v1/threads/:threadId/messages` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-thread-messages.md) for the provider-specific parameters and requirements.


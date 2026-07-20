# Langbase: List Thread Messages



```
GET https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-thread-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-thread-messages?connectionId=$CONNECTION_ID&threadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "threadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-thread-messages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threadId` | string | yes | Thread ID to list messages for. |

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

Through the native Langbase API, this operation is `GET v1/threads/:threadId/messages` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-thread-messages.md) for the provider-specific parameters and requirements.


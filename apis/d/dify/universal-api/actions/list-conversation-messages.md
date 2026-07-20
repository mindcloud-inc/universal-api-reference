# Dify: List Conversation Messages

Retrieves conversation messages from Dify.

```
GET https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-conversation-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-conversation-messages?connectionId=$CONNECTION_ID&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/list-conversation-messages?${params}`, {
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
| `conversationId` | string | yes | Conversation ID to list messages for. |
| `user` | string | no | User identifier. |
| `firstId` | string | no | Cursor for loading older messages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentThoughts": [
        {}
      ],
      "answer": "string",
      "conversationId": "string",
      "createdAt": 1,
      "error": "string",
      "feedback": {},
      "id": "string",
      "inputs": {},
      "messageFiles": [
        {}
      ],
      "parentMessageId": "string",
      "query": "string",
      "retrieverResources": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentThoughts` | array<object> |  |
| `answer` | string |  |
| `conversationId` | string |  |
| `createdAt` | number |  |
| `error` | string |  |
| `feedback` | object |  |
| `id` | string |  |
| `inputs` | object |  |
| `messageFiles` | array<object> |  |
| `parentMessageId` | string |  |
| `query` | string |  |
| `retrieverResources` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Dify API, this operation is `GET /messages` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversation-messages.md) for the provider-specific parameters and requirements.


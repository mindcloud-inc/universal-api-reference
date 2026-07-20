# Chaindesk: Get Conversation Messages

Retrieves messages from a Chaindesk conversation.

```
GET https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/get-conversation-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/get-conversation-messages?connectionId=$CONNECTION_ID&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/get-conversation-messages?${params}`, {
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
| `conversationId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "createdAt": "string",
      "eval": "string",
      "from": "string",
      "html": "string",
      "id": "string",
      "read": true,
      "sources": [
        "string"
      ],
      "text": "string",
      "updatedAt": "string",
      "usage": {
        "completionTokens": 1,
        "cost": 1,
        "promptTokens": 1,
        "totalTokens": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string |  |
| `createdAt` | string |  |
| `eval` | string |  |
| `from` | string |  |
| `html` | string |  |
| `id` | string |  |
| `read` | boolean |  |
| `sources` | array<string> |  |
| `text` | string |  |
| `updatedAt` | string |  |
| `usage` | object |  |
| `usage.completionTokens` | number |  |
| `usage.cost` | number |  |
| `usage.promptTokens` | number |  |
| `usage.totalTokens` | number |  |

## Native endpoint

Through the native Chaindesk API, this operation is `GET /conversations/:conversationId/messages` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation-messages.md) for the provider-specific parameters and requirements.


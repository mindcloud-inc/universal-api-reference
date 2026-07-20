# Chatvolt AI: Get one Message

Retrieves a message from Chatvolt AI.

```
GET https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-get-one-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-get-one-message?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-get-one-message?${params}`, {
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
| `messageId` | string | yes | Message ID. |
| `includeSources` | boolean | no | Include the 'sources' property in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "agentModel": "string",
      "contactId": "string",
      "conversationId": "string",
      "createdAt": "string",
      "eval": "string",
      "externalId": "string",
      "from": "string",
      "html": "string",
      "id": "string",
      "inputId": "string",
      "metadata": {},
      "read": true,
      "sources": [
        "string"
      ],
      "text": "string",
      "updatedAt": "string",
      "usage": {},
      "usageCredits": 1,
      "userId": "string",
      "visitorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | AgentId. |
| `agentModel` | string | AgentModel. |
| `contactId` | string | ContactId. |
| `conversationId` | string | ConversationId. |
| `createdAt` | string | CreatedAt. |
| `eval` | string | Eval. |
| `externalId` | string | ExternalId. |
| `from` | string | From. |
| `html` | string | Html. |
| `id` | string | Id. |
| `inputId` | string | InputId. |
| `metadata` | object | Metadata. |
| `read` | boolean | Read. |
| `sources` | array | Sources. |
| `text` | string | Text. |
| `updatedAt` | string | UpdatedAt. |
| `usage` | object | Usage. |
| `usageCredits` | number | UsageCredits. |
| `userId` | string | UserId. |
| `visitorId` | string | VisitorId. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `GET /messages/{messageId}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/conversation-get-one-message.md) for the provider-specific parameters and requirements.


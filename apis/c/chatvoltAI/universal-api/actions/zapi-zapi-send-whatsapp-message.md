# Chatvolt AI: Send WhatsApp Message

Sends a whatsApp Message through Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/zapi-zapi-send-whatsapp-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/zapi-zapi-send-whatsapp-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "instanceId": "string",
  "contactPhone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/zapi-zapi-send-whatsapp-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "instanceId": "string",
    "contactPhone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `instanceId` | string | yes | Z-API instance ID (externalId of the ServiceProvider of type 'zapi'). |
| `contactPhone` | string | yes | Recipient's WhatsApp number. |
| `message` | string | no | Textual content of the message. |
| `attachments[]` | array<object> | no | Optional list of attachments to be sent. |

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

Through the native Chatvolt AI API, this operation is `POST /zapi/{instanceId}/{contactPhone}/message` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/zapi-zapi-send-whatsapp-message.md) for the provider-specific parameters and requirements.


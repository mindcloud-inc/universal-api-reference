# Chatvolt AI: Send SMS Message

Sends an SMS message through Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/twilio-send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/twilio-send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ownerPhone": "string",
  "contactPhone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/twilio-send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ownerPhone": "string",
    "contactPhone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ownerPhone` | string | yes | The Twilio phone number that owns the integration. |
| `contactPhone` | string | yes | Recipient's phone number. |
| `message` | string | no | Textual content of the message. |

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

Through the native Chatvolt AI API, this operation is `POST /twilio/{ownerPhone}/{contactPhone}/message` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/twilio-send-message.md) for the provider-specific parameters and requirements.


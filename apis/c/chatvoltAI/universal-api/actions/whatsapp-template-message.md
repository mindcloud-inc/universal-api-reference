# Chatvolt AI: WhatsApp Template Message

Sends a WhatsApp template message through Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/whatsapp-template-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/whatsapp-template-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneNumberId": "string",
  "to": "string",
  "text": "string",
  "agentId": "string",
  "templateName": "Ava Chen",
  "templateLangCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/whatsapp-template-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneNumberId": "string",
    "to": "string",
    "text": "string",
    "agentId": "string",
    "templateName": "Ava Chen",
    "templateLangCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phoneNumberId` | string | yes | ID of the WhatsApp Business phone number |
| `to` | string | yes | Recipient's phone number with country code |
| `text` | string | yes | Message text to store in conversation history |
| `agentId` | string | yes | ID of the agent to associate with this message |
| `templateName` | string | yes | Name of the pre-approved WhatsApp template |
| `templateLangCode` | string | yes | Language code for the template |
| `defaultStatus` | string | no | The default status to set for the conversation. |
| `buttons[]` | array<object> | no | Array of buttons for the template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "channelExternalId": "string",
      "id": "string",
      "messages": [
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
| `channel` | string | Conversation channel |
| `channelExternalId` | string | External ID for the channel |
| `id` | string | Conversation ID |
| `messages` | array<object> | Messages in the conversation |

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /whatsapp/{phoneNumberId}/template-message` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/whatsapp-template-message.md) for the provider-specific parameters and requirements.


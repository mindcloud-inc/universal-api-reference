# Chatvolt AI: Send Message by Channel

Sends a message by channel through Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "value": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "value": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Type of conversation identifier. It can be "conversationId" for the conversation ID, "phone" for the phone number, or "email" for the email address. |
| `value` | string | yes | Value corresponding to the identifier type specified in "type". |
| `message` | string | yes | Content of the message to be sent. |
| `agentId` | string | no | (Optional) Agent ID, in cuid format. |
| `channel` | string | no | (Optional) Channel used to send the message. |
| `attachments[]` | array<object> | no | (Optional) List of attachments to be sent. |
| `visitorId` | string | no | (Optional) Visitor ID, if applicable. |
| `contactId` | string | no | (Optional) Contact ID, if applicable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | object | Message. |
| `success` | boolean | Success. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /conversation/message/{type}/{value}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/conversation-send-message.md) for the provider-specific parameters and requirements.


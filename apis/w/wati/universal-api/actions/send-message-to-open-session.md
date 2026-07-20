# Wati: Send Message to Open Session

Sends a text message in an open Wati session.

```
POST https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-message-to-open-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wati `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-message-to-open-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "whatsappNumber": "string",
  "messageText": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-message-to-open-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "whatsappNumber": "string",
    "messageText": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `whatsappNumber` | string | yes | WhatsApp phone number for the open session conversation. |
| `messageText` | string | yes | Text to send in the active session. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": {
        "conversationId": "string",
        "created": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "isOwner": true,
        "status": 1,
        "statusString": "string",
        "text": "string",
        "ticketId": "string",
        "type": "string",
        "whatsappMessageId": "string"
      },
      "ok": true,
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | object | Created WhatsApp message payload. |
| `message.conversationId` | string | Conversation identifier. |
| `message.created` | date | When the message was created. |
| `message.id` | string | Wati message identifier. |
| `message.isOwner` | boolean | Whether the message was sent by the connected account. |
| `message.status` | number | Numeric Wati message status. |
| `message.statusString` | string | Human-readable message status when present. |
| `message.text` | string | Sent message text. |
| `message.ticketId` | string | Conversation ticket identifier. |
| `message.type` | string | Wati message type. |
| `message.whatsappMessageId` | string | WhatsApp message identifier. |
| `ok` | boolean | Whether Wati accepted the session message. |
| `result` | string | Provider result summary. |

## Native endpoint

Through the native Wati API, this operation is `POST /api/v1/sendSessionMessage/:whatsappNumber` (base URL `{{credentials.apiEndpointUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message-to-open-session.md) for the provider-specific parameters and requirements.


# Wati: Send Interactive Buttons Message

Sends an interactive button message in Wati.

```
POST https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-interactive-buttons-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wati `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-interactive-buttons-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "whatsappNumber": "string",
  "body": "string",
  "buttons[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-interactive-buttons-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "whatsappNumber": "string",
    "body": "string",
    "buttons[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `whatsappNumber` | string | yes | Target recipient phone number. |
| `header` | object | no | Optional interactive header payload. |
| `body` | string | yes | Body text for the interactive message. |
| `footer` | string | no | Optional footer text for the interactive message. |
| `buttons[]` | array<object> | yes | Interactive button definitions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "message": {
        "conversationId": "string",
        "created": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "interactiveData": {},
        "status": 1,
        "statusString": "string",
        "text": "string",
        "ticketId": "string",
        "type": "string"
      },
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> | Provider validation errors when present. |
| `message` | object | Created WhatsApp message payload. |
| `message.conversationId` | string | Conversation identifier. |
| `message.created` | date | When the message was created. |
| `message.id` | string | Wati message identifier. |
| `message.interactiveData` | object | Interactive payload returned by Wati. |
| `message.status` | number | Numeric Wati message status. |
| `message.statusString` | string | Human-readable message status. |
| `message.text` | string | Rendered message text. |
| `message.ticketId` | string | Conversation ticket identifier. |
| `message.type` | string | Wati message type. |
| `ok` | boolean | Whether Wati accepted the interactive buttons message. |

## Native endpoint

Through the native Wati API, this operation is `POST /api/v1/sendInteractiveButtonsMessage` (base URL `{{credentials.apiEndpointUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-interactive-buttons-message.md) for the provider-specific parameters and requirements.


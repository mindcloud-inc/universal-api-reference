# Messaggio: Send WhatsApp Template

Creates a WhatsApp template message in Messaggio.

```
POST https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/send-whatsapp-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Messaggio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/send-whatsapp-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipientPhone": "string",
  "senderCode": "string",
  "templateId": "string",
  "language": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/send-whatsapp-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipientPhone": "string",
    "senderCode": "string",
    "templateId": "string",
    "language": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipientPhone` | string | yes | Recipient phone number in international format without a plus sign. |
| `senderCode` | string | yes | WhatsApp sender code from the Messaggio project. |
| `templateId` | string | yes | Approved WhatsApp template identifier in Messaggio. |
| `language` | string | yes | Template language code, such as en. |
| `bodyParam1` | string | no | First optional template body parameter. |
| `bodyParam2` | string | no | Second optional template body parameter. |
| `urlParameter` | string | no | Optional dynamic URL parameter for a template URL button. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accepted_at": "string",
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
| `accepted_at` | string | Timestamp when Messaggio accepted the send request. |
| `messages` | array<object> | Per-recipient send results returned by Messaggio, including recipient, message_id, or error. |

## Native endpoint

Through the native Messaggio API, this operation is `POST /send` (base URL `https://msg.messaggio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-whatsapp-template.md) for the provider-specific parameters and requirements.


# Messaggio: Send WhatsApp Text

Creates a WhatsApp text message in Messaggio.

```
POST https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/send-whatsapp-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Messaggio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/send-whatsapp-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipientPhone": "string",
  "senderCode": "string",
  "messageText": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/send-whatsapp-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipientPhone": "string",
    "senderCode": "string",
    "messageText": "string"
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
| `messageText` | string | yes | WhatsApp session message text. |

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

Through the native Messaggio API, this operation is `POST /send` (base URL `https://msg.messaggio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-whatsapp-text.md) for the provider-specific parameters and requirements.


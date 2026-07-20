# Messaggio: Send Viber Text

Creates a Viber text message in Messaggio.

```
POST https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/send-viber-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Messaggio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/send-viber-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipientPhone": "15551234567",
  "senderCode": "VIBERCODE",
  "messageLabel": "promotion",
  "messageText": "Your Viber message"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/send-viber-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipientPhone": "15551234567",
    "senderCode": "VIBERCODE",
    "messageLabel": "promotion",
    "messageText": "Your Viber message"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipientPhone` | string | yes | Recipient phone number in international format without a plus sign. Example: `15551234567`. |
| `senderCode` | string | yes | Viber sender code from the Messaggio project. Example: `VIBERCODE`. |
| `messageLabel` | string | yes | Viber message label. Use promotion or transaction. Example: `promotion`. |
| `messageText` | string | yes | Viber message text. Example: `Your Viber message`. |

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

Through the native Messaggio API, this operation is `POST /send` (base URL `https://msg.messaggio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-viber-text.md) for the provider-specific parameters and requirements.

